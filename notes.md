### Commands and Comments
1. Build automation using make
2. To use a custom domain with GitHub Pages, you need to put the domain of your site (e.g., blog.example.com) inside a CNAME file at the root of your site. To do this, create the content/extra/ directory and add a CNAME file to it. Then use the STATIC_PATHS setting to tell Pelican to copy this file to your output directory. For example:  
    ~~~python   
    STATIC_PATHS = ['images', 'extra/CNAME']
    EXTRA_PATH_METADATA = {'extra/CNAME': {'path': 'CNAME'},}
    ~~~

3. Add google analytics
4. themes to tryout
    - elegant, Flex, html5-dopetrope, pelican-blue, pelican-striped-html5up, fresh
    - 
5. Plugins
    - English & Telugu versions
        http://smartass101.github.io/pelican-plugins/
        http://smartass101.github.io/pelican-plugins/category/i18n_subsites.html

6. Search functionality - google custom search vs tipue 

7. Template for the article

8. DEFAULT_LANG

9. choosing custom domain

10. source in master & content in gh-pages

11. add themes and plugins as submodules 

12. Decide on genres(tags) - inspirational, devotional, classic, trending, actor/actresses.. 

13. Viewers comments, requests - staticman vs Disqus

14. Separate authors

15. git hooks - post-commit:  `pelican content -o output -s pelicanconf.py && ghp-import output && git push origin ˓→gh-pages`

16. Trailing '\' in the urls

17. Steps to include tipue_search

18. create a new theme & add it as submodule 

19. Logo - try wix

20. travis-ci build automation

21. use of git hooks

23. Add tags to articles - externally (like 'trending')

### Todo:
1. Add gitsubmodule for pelican plugins & themes
1. Using make
    ~~~sh 
    - help:
        @echo 'Makefile for a pelican Web site                                           '
        @echo '                                                                          '
        @echo 'Usage:                                                                    '
        @echo '   make html                           (re)generate the web site          '
        @echo '   make clean                          remove the generated files         '
        @echo '   make regenerate                     regenerate files upon modification '
        @echo '   make publish                        generate using production settings '
        @echo '   make serve [PORT=8000]              serve site at http://localhost:8000'
        @echo '   make serve-global [SERVER=0.0.0.0]  serve (as root) to $(SERVER):80    '
        @echo '   make devserver [PORT=8000]          serve and regenerate together      '
        @echo '   make ssh_upload                     upload the web site via SSH        '
        @echo '   make rsync_upload                   upload the web site via rsync+ssh  '
        @echo '   make github                         upload the web site via gh-pages   '
        @echo '                                                                          '
        @echo 'Set the DEBUG variable to 1 to enable debugging, e.g. make DEBUG=1 html   '
        @echo 'Set the RELATIVE variable to 1 to enable relative urls                    '
        @echo '                                                                          '
    ~~~


    ~~~sh
    @ ~/coding/pages_github/maatemantram.github.io
    $ `make html`
    ~~~
    > command output:  
    pelican /Users/kishored/coding/pages_github/maatemantram.github.io/content -o /Users/kishored/coding/pages_github/maatemantram.github.io/output -s /Users/kishored/coding/pages_github/maatemantram.github.io/pelicanconf.py  
        Done: Processed 27 articles, 0 drafts, 0 pages, 0 hidden pages and 0 draft pages in 0.92 seconds.  
    - static files are generated in `output` directory   

    $ `make publish `

    $ `make github`
## References 
1. https://github.com/getpelican/pelican-plugins
