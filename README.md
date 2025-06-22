# Artificial Intelligence Project 2 - Backpack Prediction

> Curricular Unit: [Artificial Intelligence](https://sigarra.up.pt/feup/en/UCURR_GERAL.FICHA_UC_VIEW?pv_ocorrencia_id=541894)<br>
> Faculty: [FEUP](https://sigarra.up.pt/feup/en/web_page.Inicial)<br>
> Professor: [Pedro Mota](https://sigarra.up.pt/feup/en/func_geral.formview?p_codigo=671784)<br>
> Authors: [Bruno Oliveira](https://github.com/Process-ing), [Henrique Fernandes](https://github.com/HenriqueSFernandes), [Rodrigo Silva](https://github.com/racoelhosilva)<br>
> Final Grade: 20.0/20<br>

## Usage

All the instructions on how to run the project are documented in the notebook `proj.ipynb`.

The setup involves creating a Python virtual environment, installing the required packages, creating the Kaggle credentials and downloading the dataset.

## Tips and Tricks (for anyone doing a similar project)

- If you are still choosing a theme, see for the available options if the problem has already good solutions (F1-scores above 0.9 or low R2-scores) and if the dataset is not too big (so you can run it on your PC). Our dataset was already quite big (which is not really an issue by working with a sample) but the dataset, which ironically has a maximum quality score on Kaggle, is absolutely terrible: the best solution in Kaggle has a root mean squared error (RMSE) of 38.6 (since this is a regression problem), but you can achieve a RMSE of 39.0 just by predicting the mean... This cases always lead to very uninteresting results, and also make interpreting results harder, so we recommend avoiding them.
- Be mindful that we solved this problem as a regression problem, as a requests from our professor. Normally, *it is asked to convert regression problems into classification problems*, which will be probably your case if your problem in Kaggle is a regression problem (you have been warned)!
- We tried to use both Git and Google Colab for collaboration, and both have severe limitations. When we tried Git, it did the very annoying thing of accusing conflicts on every merge for the notebook file, since every time you run (or even switch between PCs) a lot of metadata changes (which is irrelevant for the project). Google Colab at least did not deal with this, but not only was it considerably slower than running the notebook locally, but it also had the horrible habit of rejecting some changes of some people when editing concurrently (which was really, REALLY annoying on the last day of submission). Since we don't recommend using either, there is also the option of using Kaggle notebooks, which we didn't really give it a try, so maybe start with that to see if it isn't as cumbersome as the other two.
- Some PCs (like mine) didn't like very well using `scikit-learn` with multithreading (frequently crashing). Fortunately, this was really easy to solve by using the `joblib` library and using multithreading backends: not only did it solve the crashing, but it also made parallelization run faster.
- Using AI tools for writing the text and code, and choosing parameters for each model, is actually really useful, but always don't forget to document really well each detail in the Exploratory Data Analysis (EDA) and Model Selection (and others), as AI tools normally make really generic descriptions (and you will be penalized for that).