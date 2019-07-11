# dionysus

a super basic flask starter kit made based off work from my [softdev2 final project (catatonic cereal)](https://github.com/tfabiha/ccereal/) and the [readme](https://github.com/rachel-ng/group-d-etat) from my [softdev1 final project (ambrosia)](https://github.com/rachel-ng/group-d-etat)  
<sub>so i can live my best life</sub>

also comes with recommendations for some of my school work (stuy softdev + ai mainly) with some pretty important / useful concepts for easy relearning! 

## Features (aka *The Good Stuff<!-- $#!+-->™*)

<!-- For a list of in progress<sup>*(ish)*</sup> features, [refer to this](#to-do) -->

- python3, html, css, etc. 
- [semi decent readme](#sample.md) to base stuff off of  
    <sup>if you need to do the whole *documentation thing*</sup>
- [.gitignore](.gitignore) (it's also a [gist](https://gist.github.com/rachel-ng/7e26de56cb4a6370164213bd33c31f54))
- [flask](http://flask.pocoo.org/)
    - [flash](http://flask.pocoo.org/docs/1.0/patterns/flashing/) `categories`  
      e.g. `flash("Error: Invalid Location", category="location")`  
      <sub>Refer to [lines 62-86](https://github.com/rachel-ng/dionysus/blob/master/templates/base.html#L62-L86) of [base.html](templates/base.html) for more details on implementation</sub>
- [jinja2](http://jinja.pocoo.org/) (for templating)
- [sqlite](https://docs.python.org/3.4/library/sqlite3.html) (DBs, for python functions see [config.py](util/config.py) and [db.py](util/db.py))  
    [config.py](util/config.py) uses `os` for absolute paths  
    <sup>so it doesn't go to *absolute hell* when you try to make it compatible with apache or something</sup>  
- accounts
    - stored in [data.db](data/data.db)
    - [db.py](util/db.py): functions for account creation and authentication
    - login, signup, logout (via sessions, POST)
    - password hashing (via `passlib`, uses `sha256_crypt`)
- [bootstrap](https://getbootstrap.com/)  
    <sup>psst... you just copy and paste a bunch of stuff and change the html as needed, and use custom css and stuff to make it look pretty / the way you want it to</sup>
- custom css and js  
    <sup>js file is empty btw</sup>  
    ```
    static/css/base.css
    
    <link rel="stylesheet" href="{{ url_for('static', filename='css/base.css') }}">
    ```
    ```
    static/js/my.js
    
    <script src="{{ url_for('static', filename='js/my.js') }}"></script>
    ```


## Usage

attain the files somehow (fork, download, clone repo and move files, idk it's up to you) and alter them to your choosing

### Important Files

For a full list of features, refer to [the above](#the-good-)

- sample [README.md](sample.md)
- `util/config.py` contains functions for configuring your database  
    you may choose to change the [directory](https://github.com/rachel-ng/dionysus/blob/master/util/config.py#L8) your database is in ( `data/` ) and/or the [db file's name](https://github.com/rachel-ng/dionysus/blob/master/util/config.py#L9) ( `data/data.db` )
- `util/db.py` contains functions for account creation and authentication
- `templates/base.html` the og jinja base html


### requirements.txt

0. PRE-REQ: You need to be in your virtual environment (venv).  
<sup>Follow the [instructions here](sample.md#dependencies) if you don't have a virtual environment</sup>

1. In the root of your repo, run this: 

    ```
    (venv) $ pip freeze > requirements.txt
    ```
    
    This takes a "snapshot" of all your python packages and versions installed within your virtual environment and lists them in your [requirements.txt](requirements.txt) and allows users to run your program on their own computer without worrying about compatibility issues. 
    
2. You can now use your requirements.txt by running the following command: 
    ```
    (venv) $ pip install -r requirements.txt
    ```


### README.md

- [Github's guide](https://guides.github.com/features/mastering-markdown/) to Github flavored markdown
- [adam-p](https://github.com/adam-p)'s [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)


## Recommendations

<sup>dear future me: \*taps microphone\* *listen up*</sup>

Some helpful resources in vaguely chronological order.  
<sup>projects, then useful repos / folders / links</sup>

- [softdev1 Bourbon Chocolate-Blog](https://github.com/dkeriazisStuy/Bourbon-Chocolate_Blog) (ft. daniel keriazis' frankly kinda godly work)
- [softdev1 daily updates thingy](https://github.com/ryan-aday/RanQuoR-Turkey--adayR-mohriC-ngR-zhouQ) (ft. flash categories, some weird GET stuff, *just vaguely useful*)
- [the best readme](https://github.com/rachel-ng/group-d-etat) (softdev1 final project ([ambrosia](https://github.com/rachel-ng/group-d-etat)))
- [softdev2 final project (catatonic cereal)](https://github.com/tfabiha/ccereal/)

<br>

- [stuy softdev notes and code repo](https://github.com/stuy-softdev/notes-and-code) (only if you're a member of the organization though rip)
- [softdev1 repo](https://github.com/rachel-ng/softdev)
- [softdev2 repo](https://github.com/rachel-ng/re-softdev)  
    there's also some mongoDB stuff, but that was honestly a godawful nightmare 
    - all the listcomp examples are good, but [this one utilizes them to check passwords](https://github.com/rachel-ng/re-softdev/blob/master/16_listcomp/listcomp.py) ([16_listcomp](https://github.com/rachel-ng/re-softdev/blob/master/16_listcomp/listcomp.py)) so it's more relevant
        - [17_listcomp](https://github.com/rachel-ng/re-softdev/blob/master/17_listcomp/work.py) (some practice with listcomps), [18_listcomp](https://github.com/rachel-ng/re-softdev/blob/master/18_listcomp/pyth.py) (pythagorean theorem with listcomps), [19_listcomp](https://github.com/rachel-ng/re-softdev/blob/master/19_listcomp/sets.py) (trying to replicate sets with listcomps)
    - [20_anon-reduce](https://github.com/rachel-ng/re-softdev/blob/master/20_anon-reduce/reduce.py)  
        <sup>python reduce, lambda, and my personal favorite: *list comprehensions* in a (more) easily digestable example (last function is super slow though, don't bother with it please)</sup>
    - [21_js-mfr](https://github.com/rachel-ng/re-softdev/blob/master/21_js-mfr/index.js)  
        <sup>js reduce, map, and filter functions and a XMLHttpRequest for reading a JSON that works for once</sup>
    - [22_closure](https://github.com/rachel-ng/re-softdev/blob/master/22_closure/closure.py)  
        <sup>python function that returns a function, *probably an important cs concept that i should properly relearn*</sup>
    - [23_memoize](https://github.com/rachel-ng/re-softdev/blob/master/23_memoize/memoize.py)  
        <sub>python *time-saving solutions via closures*</sub>  
        <sup>also: according to my manager *something something fib seq something good example something O(N<sup>2</sup>) runtime to linear O(N) runtime*</sup>
- [stuy ai repo](https://github.com/rachel-ng/ai-cant-even)
    - [some python review stuff from mr. brooks](https://github.com/rachel-ng/ai-cant-even/tree/master/b_python_review)
        - [python 2.7 quick reference](http://rgruet.free.fr/PQR27/PQR2.7.html)
        - [mr. brooks' python "cribsheet"](http://bert.stuy.edu/pbrooks/cribsheets/Python-sheet.pdf)
        - [mr. brooks' python / html stuff](http://bert.stuy.edu/pbrooks/IntroResources/TOC.html)
        - ["advanced constructs"](http://bert.stuy.edu/pbrooks/IntroResources/PythonAdvancedConstructs.htm) (list comprehensions, reduce, lambda)  
            [20_anon-reduce](https://github.com/rachel-ng/re-softdev/blob/master/20_anon-reduce/reduce.py) from softdev is also a really good resource for trying to comprehend this stuff (again) 
    - [python classes](https://github.com/rachel-ng/ai-cant-even/tree/master/b_python_classes)
    - [some wild list + set comprehensions from pre-wordladders](https://github.com/rachel-ng/ai-cant-even/blob/master/3_pre-wordladder/neighbors.py)
    - [an actually function a* search (code not mine)](https://github.com/rachel-ng/ai-cant-even/blob/master/0_extra_credit/wordladders_extra_credit_04_10_2019.py)
