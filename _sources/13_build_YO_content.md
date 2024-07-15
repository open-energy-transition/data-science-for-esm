<!-- # Table of Contents

1. [BYOC](#build-your-own-content)
1. [New Fork](#creating-a-new-fork)
1. [GH Pages](#gh-pages-setup)
1. [GH Workflows Deployment](#gh-workflows-deployment) -->

# Build Your Own Content

<!-- ###### List of Abbreviation[^bignote] -->

This section assists academics, and alike, in build their content, by modifying this repository, or the original [Dr. F. Neumann's repository][01].

> * Its primary purpose if helping/guiding on building a GH[^bignote] page, to be used for generating learning material, i.e. lectures, or similar.
> * It can also be used for any other purpose, for that matter.

The first step is forking this repository. By doing so, one is able to create his own website, similar to this one, with a tailor-made content, quickly and with ease.

- This setup draws from the [peaceiris actions-gh-pages][02], and the [Stanford RC website][03]. However, these serve only as a reference, as the the full explanation is blow.

# Creating a new fork

Before forking this repository please have the following in mind. In the `Create a new fork` pop-up menu, deselect the default **Copy the `main` branch only** option. By doing so, you will reduce further branch creation.

:::{note}
<center>
<figure>
    <a href='https://github.com/open-energy-transition/data-science-for-esm/fork'>
    <img src='https://github.com/open-energy-transition/data-science-for-esm/raw/stanford/data-science-for-esm/_images/03_fork_option.png' alt='' width='95%' style='vertical-align:middle;border:5px solid goldenrod;margin:20px 0px' />
    </a>
    <figcaption>Clicking on the image above will lead directly to the <b><strong><mark>Create a new fork menu</mark></b></strong></figcaption>
</figure>
</center>
:::

> The first step is forking the repository, having the <mark>**Note**</mark> above in mind.

The following steps are:
* Create and push a branch named `stanford` - to be skipped if adhering to the **Note** above
* `gh-pages` branch will be automatically generated, as defined by the workflow in the `.github/workflows/deploy.yml` ([link][07]) file which will contain the required `HTML`, `css`, `.js`, and other files
* in the `.github/workflows/deploy.yml` file you also specify the branch, used by the workflow, which upon the `git push` command, is used for generating the required `HTML`, `css`, `.js`, as well as the other files - other than the `gh-pages`:
    
    ~~~yml
    push:
      branches:
      - **stanford**
    ~~~

- in the `data-science-for-esm/_toc.yml` *file*, a sequence of files to be included in the GitHub Page is defined, thereafter displayed in the menu, located on the left side of the page
- on preexisting knowledge disseminating the gained expertise by OET, and TU Berlin, to help .   Welcome to the website accompanying the course [Data Science for Energy System Modelling][04]. This course is being developed by [Dr. F. Neumann][05] and offered as part of the curriculum of the [Department of Digital Transformation of Energy Systems at TU Berlin][06].

In the your own forked repository `owner/data-science-for-energy-system-modelling`, please go to the **Settings** -> **Pages**. in the GitHub Page, go to the Branch section, and change the selection from None to `main`, or any branch other than `gh-pages`. Once the branch has been selected, in a manner of minutes a custom  

# <font color="red">GH Pages Setup</font>

<center>
<figure>
    <a href='https://github.com/open-energy-transition/data-science-for-esm/settings/pages'>
    <img src='https://raw.githubusercontent.com/open-energy-transition/data-science-for-esm/stanford/data-science-for-esm/_images/04_gh_pages-options.png' width='97%'style='vertical-align:middle;border:5px solid goldenrod;margin:30px 30px' />
    </a>
    <figcaption>Clicking on the image above will lead directly to the GH Pages settings menu</figcaption>
</figure>
</center>

# <font color="red">GH Workflows Deployment</font>

`.github/workflows/deploy.yml` ([link][08]) needs specifying which branch of the repo will be used for deployment. You are free to use any branch, other than the `gh-pages`, keeping in mind that upon the `git push`, the workflow will be triggered.

This is indicated by the status indicator in the repository, in this case a beige-brown dot, which if clicked on, will show the running status and the deployment details. As mentioned, the deployment takes approx. 2 minutes.

<center>
<figure>
    <!-- <a href='https://github.com/open-energy-transition/data-science-for-esm/settings/pages'> -->
    <img src='https://raw.githubusercontent.com/open-energy-transition/data-science-for-esm/stanford/data-science-for-esm/_images/05_deployment_status.png' width='85%'style='vertical-align:middle;border:5px solid paleturquoise;margin:30px 30px' />
    <!-- </a> -->
    <figcaption>Deployment status upon <mark>git push</mark> to the branch specified in the <em>deploy.yml</em> file</figcaption>
</figure>
</center>

Upon a successful deployment, indicated by the deploy status, in that time you should be able to see the changes taking place in the specified `github.io` URL.

<center>
<figure>
    <!-- <a href='https://github.com/open-energy-transition/data-science-for-esm/settings/pages'> -->
    <img src='https://raw.githubusercontent.com/open-energy-transition/data-science-for-esm/stanford/data-science-for-esm/_images/06_successful_deployment.png' width='85%'style='vertical-align:middle;border:5px solid paleturquoise;margin:30px 30px' />
    <!-- </a> -->
    <figcaption>Successful deployment, after a finalized <b>jupyter book build</b> run</figcaption>
</figure>
</center>

<!-- # References -->
[01]: https://github.com/fneum/data-science-for-esm
[02]: https://github.com/peaceiris/actions-gh-pages
[03]: https://stanford-rc.github.io/rse-services/docs/resources/documentation
[09]: https://github.com/open-energy-transition/data-science-for-esm/fork
[10]: https://github.com/open-energy-transition/data-science-for-esm/settings/pages
[04]: https://moseskonto.tu-berlin.de/moses/modultransfersystem/bolognamodule/beschreibung/anzeigen.html;jsessionid=DQfixqzzpn1XIg5N1GG7S9um4EDykZn99AHmH6Fj.moseskonto?number=31027&version=1&sprache=2
[05]: https://neumann.fyi
[06]: https://www.tu.berlin/ensys
[07]: https://github.com/open-energy-transition/data-science-for-esm/blob/ef394898e3100e2bd2d074a8b2da89235355cd4e/.github/workflows/deploy.yml
[08]: https://github.com/open-energy-transition/data-science-for-esm/blob/6c6563e15d3035647e9e52c852fa1cd5748f15ed/.github/workflows/deploy.yml#L4C2-L7C15

<center><mark>Table of Abbreviations</mark></center>

[^bignote]:
 | Acronym     | Description |
 |:-----------:|:-----------:|
 | **GH**      | GitHub      |
 | **repo**    | repository  |