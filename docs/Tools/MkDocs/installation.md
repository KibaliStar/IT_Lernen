# MkDocs Installation

[:simple-youtube: Material for MkDocs: Full Tutorial To Build And Deploy Your Docs Portal](https://www.youtube.com/watch?v=xlABhbnNrfI){: target="_blank" }

[:simple-materialformkdocs: Material for MkDocs ](https://squidfunk.github.io/mkdocs-material/reference/){: target="_blank" }

``` py
    # im VS Terminal
    python -V                  # Python 3.13.5
    pip --version              # pip 25.1.1
    python -m venv venv
    source venv/bin/activate   # windows: .\venv\scripts\activate

    pip install mkdocs-material

    code .                     # VS Code öffnet sich in diesem Verzeichniss

    mkdocs new .               # INFO    -  Writing config file: .\mkdocs.yml
                            # INFO    -  Writing initial docs: .\docs\index.md
                            
    mkdocs serve               # Startet den Liveserver

    # VS Extensions
    #    yaml  (von Red Hat) installieren

    # VS Settings Ctrl+,
    # dann rechts oben Open Settings (JSON)
    # füge ein (https://squidfunk.github.io/mkdocs-material/creating-your-site/)
    # wenn Probleme, frag KI: 
    '''
    {
    "yaml.schemas": {
        "https://squidfunk.github.io/mkdocs-material/schema.json": "mkdocs.yml"
    },
    "yaml.customTags": [ 
        "!ENV scalar",
        "!ENV sequence",
        "!relative scalar",
        "tag:yaml.org,2002:python/name:material.extensions.emoji.to_svg",
        "tag:yaml.org,2002:python/name:material.extensions.emoji.twemoji",
        "tag:yaml.org,2002:python/name:pymdownx.superfences.fence_code_format",
        "tag:yaml.org,2002:python/object/apply:pymdownx.slugs.slugify mapping"
    ]
    }
    '''

    mkdocs.yml                  # Einstellungen, Colorchema, Nav, Search uvm.

    # im VS-Terminal
    git init

    # .gitignore anlegen

    # im VS-Terminal
    git add .
    git status
    git commit -m "Initial commit"
    git remote add origin https://github.com/KibaliStar/IT_Lernen.git
    git push origin master

    # in Github Settings musste der Default branch von main auf master umgestellt werden, 
    # nun sind die Dat. auf Guthub sichtbar

    # Github General/DangerZone auf Publich setzen wenn noch nicht geschehen
    # Github  Setings/Pages  Branch auf gh-pages, Save
    # Github Actions (oben), (page build and deployment)
    # deploy zeigt link an, hier: https://kibalistar.github.io/IT_Lernen/

    pip install mkdocs-glightbox           # für Bilder
    pip install mkdocs-breadcrumbs-plugin  # für Breadcrumbs
```