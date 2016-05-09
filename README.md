- [README](#readme)
  - [Introduce](#introduce)
  - [Install](#install)
  - [Configure](#configure)
  - [Usage](#usage)

# README<a id="org4afe163"></a>

## Introduce<a id="orgbf07d29"></a>

ebib-handy is a ebib tool, which can let ebib become a cite chooser.
![img](./snapshots/ebib-handy.gif)

## Install<a id="orgb0d2702"></a>

1.  Config melpa: <http://melpa.org/#/getting-started>
2.  M-x package-install RET ebib-handy RET
3.  Add code to your emacs config <（for> example: ~/.emacs）：

## Configure<a id="orgffe8b0d"></a>

    (require 'ebib-handy)
    (ebib-handy-enable)

    (require 'org)
    (org-add-link-type "cite" 'ebib-handy) ;org cite link setting
    (setq ebib-extra-fields
          '((BibTeX "keywords" "abstract" "timestamp"
                    "file"  "url" "crossref" "annote" "doi")
            (biblatex "keywords" "abstract" "timestamp"
                      "file"  "url" "crossref" "annote" "doi")))

## Usage<a id="orgca542de"></a>

    (global-set-key "\C-c b" 'ebib-handy)

You can open "example/thesis.org" then type 'C-c b'.
