My notes on setting up GitHub Pages utilizing Jekyll.

# Install Jekyll

- <https://jekyllrb.com/docs/installation/>
- <https://jekyllrb.com/docs/installation/macos/>

~Note~: Currently `brew install chruby ruby-install; ruby-install ruby` does not work with the latest macOS! So I tried `brew install ruby`.

```bash
> homebrew intall ruby
> ruby -v
ruby 2.6.10p210 (2022-04-12 revision 67958) [universal.x86_64-darwin22]
> gem install jekyll bundler
```

Align environment!

```bash
[... .zshrc ...]
RUBY_HOME="/usr/local/Cellar/ruby/3.1.2_1"
RUBY_BIN=${RUBY_HOME}/bin
# For compilers to find ruby you may need to set:
export LDFLAGS="-L${RUBY_HOME}/lib"
export CPPFLAGS="-I${RUBY_HOME}/include"

BIN_PATH=${RUBY_BIN}:\${HOME}/.local/bin:\...
export PATH=$BIN_PATH:$PATH
```

# Test GitHub Pages site locally

<https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll>

```
> jekyll new <project>
> cd <project>
> [vim Gemfile and add `gem "webrick"`
> bundle install
> bundle exec jekyll serve --livereload
> open http://localhost:4000
```

# Create a GitHub repository

https://docs.github.com/en/pages/quickstart
