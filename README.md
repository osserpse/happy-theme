happy-theme
===========

Tema att använda tillsammans med Octopress. För internt bruk för Happy User, den skapar ett tema som jag använder för Style Guides i projekt.

## Installation

*1. Installera för Octopress* Kortversionen, långa versionen på http://octopress.org/docs/setup/

```
cd <där du vill ha projektet>
git clone git://github.com/imathis/octopress.git <projekt-namn>
cd <projekt-namn>    # If you use RVM, You'll be asked if you trust the .rvmrc file (say yes).
ruby --version  # Should report Ruby 1.9.3
```

Next, install dependencies.

```
gem install bundler
bundle install
```

Install the default Octopress theme.

```
rake install
```

*2. Skapa deploy till Heroku* Kortversion, långa versionen på http://octopress.org/docs/deploying/heroku/

```
gem install heroku
heroku create
# Set heroku to be the default remote for push/fetch
git config branch.master.remote heroku
```

Edit the .gitignore in the root of your repository and remove public. This will let you add generated content for deploying it to Heroku.

```
rake generate
git add .
git commit -m 'Initial commit'
git push heroku master
```

*3. Installera tema*

```
$ cd <projekt-namn>
$ git clone git://github.com/osserpse/happy-theme.git .themes/happy-theme
$ rake install['happy-theme']
# Här får man frågan om man vill skriva över installerat tema
#   Svara definitivt "ja" första gången, men var försiktig sedan
#   och kontrollera att inte ändringar skett i befintliga tema-filer
$ rake generate
```


