# Git Celebration Sounds

Following on from a blog post on [happy git commits][hgc], I pulled together a bunch of `.wav` files from voice commands in the game [TF2][] to use as well. `post-commit` (and `post-update`) scripts just play one of the files at random.

[hgc]: http://tf2wiki.net/wiki/Main_Page
[TF2]: http://www.teamfortress.com/

## Installation

	git clone git://github.com/caius/git-celebration-sounds.git ~/.git

Then in each git repo you want the sounds to play, I symlink in the post-commit/update scripts.

	cd $repo
	ln -s ~/.git/hooks/post-{commit,update} .git/hooks

I've wrapped that into a git alias to run it easily for each new git repo.

	git config --global alias.happify '!sh -c "ln -s ~/.git/hooks/post-{commit,update} .git/hooks"'

Then it's just a simple `git happify` in a repo to link the hooks in.

(Also see the original [blog post][hgc] for ideas on doing it automatically in a new git repo.)

## Sound attributions

* `happykids.wav` comes from <http://collectiveidea.com/blog/archives/2010/08/03/happy-git-commits/>
* All the other wav's come from the tf2 wili - <http://tf2wiki.net/wiki/Main_Page>

