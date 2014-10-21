Motivation?
-----------
First I thought of making a blog-ish thingy I was going to use WordPress, then I thought I have to go through all that trouble to set it up and stuff. So I didn't want to host it on WordPress. Not that this is any easier to set up.

I think I would learn something if I tried Jekyll, this for me was kind of a cross between a full fledge site-on-server and a full fledge blogging service. (Like how I picked tumblr. as it as a cross between a blog and a microblog). Jekyll, as part of a Ruby gem, which is also something I never touched, is also something new to me. Maybe I'll learn about it? or maybe not.

The decisions are set, may as well do it, try something new.
(I also thought this was a good time for me to learn how to write markdown, though it seems like LaTeX is the shit now, but those are completely for differenet usage! What am I saying).

From Setting Up Server to Deploying
-----------------------------------
### Prologue ###
Ruby... apparently doesn't play nice with Windows, which is my host machine. Jekyll is not officially supported on Windows. Though there are ways of getting it on it, but I thought screw it, I'll just install it on a vm or something.

As of now, I didn't install it on a vm, instead I created a digital ocean droplet, and I'm making everything there. With the idea of I can access it anywhere as long as I have a terminal. I guess this also goes true that I am hosting it on github, I can just go on github and modify a file or too. (Not like I can't access WordPress from anywhere =__=) I'm just being difficult.

I created a few droplets before I settled on this one. It uhhhh, wasn't too easy. I started with Jekyll-Bootstrap, but later I decided just to go with Jekyll, which is probably not the easiest thing to start with and definitely harder than Jekyll-Bootstrap, but I thought it might be an interesting experience after all.

### Set Up ###
I started with a generic Ubuntu droplet, I tried the ruby-on-rails droplet. I, being difficult again, thought it was too much hand holding, decided to make a droplet able to run Jekyll by myself. (I'm shameless to even write about this)

First thing I needed was Ruby, and obviously (as I didn't know) apt-get wasn't good enough. I can get ruby, but I have build problems when I try to get the Jekyll gem. eventually I decided to use RVM, that, worked like a charm.
Now I finally acquired Ruby and Jekyll, and bundle

### Trying to run Jekyll ###
Now that I have Jekyll, and ruby, time to run it!
`bundle exec jekyll serve`
It didn't work, what was I thinking, but what is this `ExecJS::RuntimeUnavailable`? No JS runtime? )= After Googling it appears I need `execjs` and `therubyracer` in my `GemFile`, so I did that and it worked, yay. But wait, do I have to have it in all my GemFiles forever? Further Googling teels me I can just install `nodejs`, wait wut? I thought this was a ruby thing. Something tells me there's another way of doing this, if anyone knows, help me out.
But once I had my js runtime, I can finally see the page.

### Deploying to github ###
Obviously this thing needs to be hosted somewhere, and another good reason I would like to use Jekyll is that I can host it on github, as of my homepage.

Need to first make repo, I made mine called "blog" very creative.
Following a bunch of instructions (make gh-pages branch etc), and push! hmmm, that didn't work either. seems like my page isn't rendering correctly at all. More instructions too follow. after modifying _config.yml it rendered on github! I am also impressed on github renders pages nowadays, I remember it would take like a minute to push something and for it to display on the site a few years back, without Jekyll too. Now I have Jekyll setup!

From Themes to First (or Second) Blog
-------------------------------------

### Themes ###
[Jekyll Themes](http://jekyllthemes.org/) were found with ease, and from a list of themes I decided to use [Shiori](http://jekyllthemes.org/themes/shiori/), seemed like a clean and simple theme that doesn't tire the eye. Follow by that instruction I should have forked and made the blog based on that. I guess I may as well do that. Destroy my old repo, fork her repo, clone, and rebundle.
I never contributed to any project before either, so forking and staying up to date with the remote was also something new to me, that was also an experience.
That's how I ended up with this theme

### Writing blog ###
This is my second blog, I haven't wrote the first one as of yet because I'll be adding more to this one.
Writing in md, may be a cool experience, as I am just writing without looking at what it will look like yet. =S
Hope it ends well.
