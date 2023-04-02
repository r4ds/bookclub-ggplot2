# R4DS ggplot2 Book Club

Welcome to the R4DS ggplot2 Book Club!

We are working together to read [ggplot2: Elegant Graphics for Data Analysis](https://ggplot2-book.org/index.html) by Hadley Wickham, Danielle Navarro, and Thomas Lin Pedersen.
Join the [#book_club-ggplot2](https://rfordatascience.slack.com/archives/C025VADE84A) channel on the [R4DS Slack](https://r4ds.io/join) to participate.
As we read, we are producing [notes about the book](https://r4ds.github.io/bookclub-ggplot2/).

## Meeting Schedule

If you would like to present, please see the sign-up sheet for your cohort (linked below, and pinned in the [#book_club-ggplot2](https://rfordatascience.slack.com/archives/C025VADE84A) channel on Slack)!

- Cohort 1 (started 2021-08-30, ended 2022-07-18): [meeting videos](https://www.youtube.com/playlist?list=PL3x6DOfs2NGhUxGvu46tXQtBl0qyTcDet)
- [Cohort 2](https://docs.google.com/spreadsheets/d/1Wt3F_xh45__Zp1Q4v_BJ9jH64el2MHji7sx1tVzCrCU/edit?usp=sharing) (started 2023-04-06): [Thursdays, 08:00pm CST/CDT](https://www.timeanddate.com/worldclock/converter.html?iso=20230407T010000&p1=24&p2=179&p3=tz_ist&p4=1440) | [meeting videos](https://youtube.com/playlist?list=PL3x6DOfs2NGhw3rkmaGipc21j0a7sCPNy)

## How to Present

This repository is structured as a [{bookdown}](https://CRAN.R-project.org/package=bookdown) site.
To present, follow these instructions:

Do these steps once:

1. [Setup Github Locally](https://www.youtube.com/watch?v=hNUNPkoledI) (also see [_Happy Git and GitHub for the useR_](https://happygitwithr.com/github-acct.html))
2. Install {usethis} and {devtools} `install.packages(c("usethis", "devtools"))`
3. Set up a default {usethis} directory:
  - `usethis::edit_r_profile()` to open your profile for editing.
  - Add this line: `options(usethis.destdir = "YOURDIR")` (replace `YOURDIR` with the root directory under which you want your R projects to appear; or you can skip these steps, and the project will be saved to your Desktop).
  - Restart your R session (Session/Restart R in Rstudio).
4. `usethis::create_from_github("r4ds/bookclub-ggplot2")` (cleanly creates your own copy of this repository).

Do these steps each time you present another chapter:

1. Open your project for this book.
2. `usethis::pr_init("my-chapter")` (creates a branch for your work, to avoid confusion, making sure that you have the latest changes from other contributors; replace `my-chapter` with a descriptive name, ideally).
3. `devtools::install_dev_deps()` (installs any packages used by the book that you don't already have installed).
4. Edit the appropriate chapter file, if necessary. Use `##` to indicate new slides (new sections).
5. If you use any packages that are not already in the `DESCRIPTION`, add them. You can use `usethis::use_package("myCoolPackage")` to add them quickly!
6. Build the book! ctrl-shift-b (or command-shift-b) will render the full book, or ctrl-shift-k (command-shift-k) to render just your slide. Please do this to make sure it works before you push your changes up to the main repo!
7. Commit your changes (either through the command line or using Rstudio's Git tab).
8. `usethis::pr_push()` (pushes the changes up to github, and opens a "pull request" (PR) to let us know your work is ready).
9. (If we request changes, make them)
10. When your PR has been accepted ("merged"), `usethis::pr_finish()` to close out your branch and prepare your local repository for future work.
11. Now that your local copy is up-to-date with the main repo, you need to update your remote fork. Run `gert::git_push("origin")` or click the `Push` button on the `Git` tab of Rstudio.

When your PR is checked into the main branch, the bookdown site will rebuild, adding your slides to [this site](https://r4ds.github.io/bookclub-URL/).
