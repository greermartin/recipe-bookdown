# TEACHxperts Workshop Instructions

## Beginner: Instructions for anyone who is new to GitHub or R Studio

These instructions require a web browser. No software installations are necessary.

1. Create a free GitHub account: https://github.com/
2. While logged in, visit: https://github.com/chrisdaaz/recipe-bookdown
3. At the top-right of the page, click on the `Fork` button:

![image](https://user-images.githubusercontent.com/24395592/73391514-bf991200-429d-11ea-9299-7946b6d71662.png)

_This action will create a copy of the project files for you to edit. After the copying is complete, you should now be looking at your version of the project at `https://github.com/[YOUR_USERNAME]/recipe-bookdown`_

4. Click on the `Create new file` button

![image](https://user-images.githubusercontent.com/24395592/73391559-d3dd0f00-429d-11ea-8293-6006b1e999b9.png)

5. Give the new file a name based on your recipe (e.g. `mushroom-pizza.Rmd`). It is **very** important that the file extension is `.Rmd`
6. In the `Edit new file` window, paste the following text:

```
<!-- Type:Soup -->
<!-- Cook:JEmery -->

# Title of Recipe

\begin{recipe}{title}{number of servings}{preparation time}
\freeform Add any setup instructions, such as preheating an oven.
\ingredient[Numerical quantity]{Unit of measurement}{Ingredient}
\ingredient[Numerical quantity]{Unit of measurement}{Ingredient}

Instructions for what to do with the above ingredients.

\freeform Add final notes, such as serving suggestions.
\end{recipe}
```

7. Edit the text using this as a guide:

| Line Number | Text to Edit                                                                    | Example                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1-2         | ```<!-- Type:[Type of Dish] --><br><!-- Cook:[First Initial + Last Name] -->``` | ```<!-- Type:Soup --><br><!-- Cook:JEmery -->```                                                                                       | We want to organize the book into sections based on the types of dishes and the contributors. These labels will help.                                                                                                                                                                                                                                                                                                                                                                                    |
| 4           | `# Title of Recipe`                                                             | `# Moroccan Stew`                                                                                                                      | Keep the `#` at the beginning of the line and enter the title of your recipe                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 6           | `\begin{recipe}[title]{number of services}{preparation time}`                   | `\begin{recipe}[MoroccanStew]{Moroccan Lamb (or Turkey) Stew}{4 Portions}{1 hour}`                                                     | Begin the recipe by entering the title, portions, and estimated time it takes to make.                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 7           | `\freeform Add any setup instructions, such as preheating an oven.`             | `\freeform Preheat oven to 450 degrees F.  Line baking sheet with parchment paper or foil.`                                            | Add any set-up instructions, advice, or suggestions you have before someone begins making the recipe.                                                                                                                                                                                                                                                                                                                                                                                                    |
| 8+          | `\ingredient{Numerical quantity}{Unit of measurement}{Ingredient}`              | ```\ingredient[2]{cups}{onion}<br><br>\ingredient[\fr12]{cup}{carrots}<br>\ingredient[2-3]{}{overripe bananas}```                      | Add a line for an ingredient: start with the name of the ingredient, the numerical quanity, and unit of measurement (optional). For any step in the cooking process, you can add multiple ingredients following the same pattern. If you're adding fractions, prepend `\fr` to the numerator, followed immediately by the denominator. For example: `\fr12` will render one half, while `\fr34` will render as three-fourths. You can skip a unit of measurement by including empty curly brackets `{}`. |
| 11+         | `Instructions for what to do with the above ingredients.`                       | Add oil to pan. Chop onions vertically and carrots diagonally. Add to pan and saut\'{e} for 4-5 minutes on medium heat, or until soft. | Explain this step in the cooking process in relation the ingredients mentioned above.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 13          | `\freeform Add final notes, such as serving suggestions.`                       | `\freeform Allow to cool before serving, about 10 minutes.`                                                                            | Include any final notes to the reader, including serving suggestions and pairings.                                                                                                                                                                                                                                                                                                                                                                                                                       |

8. Add as many steps and ingredients as you need. Just make sure that the last line in the file is this: `\end{recipe}`
9. When you are ready to save the file, scroll to the bottom of the page and fill out the form with the following information: the name of the edit (e.g. `Adds pizza recipe`) and add an optional description of the edit/
10. Keep the setting on: `Commit directly to the master branch`
11. Click on the `Commit changes` button
12. Go back to the original repository: https://github.com/chrisdaaz/recipe-bookdown
13. Click on `New Pull Request`

![image](https://user-images.githubusercontent.com/24395592/73391624-eeaf8380-429d-11ea-97ca-b3c57bff7043.png)

14. Click on `compare across forks`
15. We want to pull edits from the head repository (i.e. your forked repository) to the base repository (`chrisdaaz/recipe-bookdown`). In the drop-down menu, select your fork: `[YOUR_USERNAME]/recipe-bookdown`

![image](https://user-images.githubusercontent.com/24395592/73395126-7a2c1300-42a4-11ea-8b20-0764e3876604.png)

16. Click on `Create pull request`
17. Enter a name for the pull request (e.g. `Chris's Recipe`)
18. Click on `Create pull request`

_By doing this, you are requesting to have your recipe added to the shared recipe book. We will approve your request and a new version of the recipe book will be made._

**Finished!**

## Intermediate: Instructions for anyone who is familiar with GitHub and R Studio

These instructions assume you have a GitHub account and R Studio installed on your computer. We recommend using the [Bookdown](https://bookdown.org/yihui/bookdown/) manual, which is an excellence source for getting started with this package. We also highly recommend [GitHub Desktop](https://desktop.github.com/) for handling git commands.

- Sign into GitHub
- At the top-right of the page, click on the `Fork` button:

![image](https://user-images.githubusercontent.com/24395592/73391514-bf991200-429d-11ea-9299-7946b6d71662.png)

- Open [R Studio](https://rstudio.com/)
- Create a new project with version control
- Clone your forked repository via this URL(swap in your username): `https://github.com/YOUR_USERNAME/recipe-bookdown.git`
- Install bookdown: `install.packages("bookdown")`
- Create a new `.Rmd` file named after your recipe
- Follow steps 5-8 from the "Beginner" instructions
- Save the file and commit it to the master branch of your local git repository in R studio
- Push the changes from your local reository to your forked repository on GitHub
- Follow steps 12 - 18 from the "Beginner" instructions to finish adding your recipe to the book.

## Credits

This is a minimal example of a book based on R Markdown and **bookdown** (https://github.com/rstudio/bookdown). Please see the page "[Get Started](https://bookdown.org/yihui/bookdown/get-started.html)" at https://bookdown.org/yihui/bookdown/ for how to compile a **bookdown** project into HTML. You may generate a copy of the book in `bookdown::pdf_book` format by calling `bookdown::render_book('index.Rmd', 'bookdown::pdf_book')`. More detailed instructions are available here https://bookdown.org/yihui/bookdown/build-the-book.html.
