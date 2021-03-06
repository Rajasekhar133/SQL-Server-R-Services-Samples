# Galaxies classification with Deep Learning from Microsoft ML using SQL Server ML Services
This samples shows how to use deep learning and image data to classify galaxies. The scenario is specific to research but can be generalized to image classification for many other industries.
It provides the supporting SQL and R scripts for the blog post [How six lines of code + SQL Server can bring Deep Learning to ANY App](https://blogs.technet.microsoft.com/dataplatforminsider/2017/01/05/how-six-lines-of-code-sql-server-can-bring-deep-learning-to-any-app/).

**Data**: [Galaxy Zoo](https://www.galaxyzoo.org/) project was used as source of labeled training data.

**Scripts**: The following scripts are provided in the `SQLR` folder:

- `createTables.sql`: create tables for trained models and scored data.
- `train_NN_model.sql`: stored procedure for training NN model with Microsoft ML
- `predict_NN_model.sql`: stored procedure for scoring
- `trigger_predict_model.sql`: script to invoke scoring. This uses a trigger to run the scoring when a row is inserted into the `GalaxiesToScore` table.

For end-to-end training and prediction the images could be downloaded from public storage.
See this links for more info:
- [Morphological classifications of main-sample spectroscopic galaxies from Galaxy Zoo 2](http://skyserver.sdss.org/dr13/en/help/browser/browser.aspx#&&history=description+zoo2MainSpecz+U)
- [Galaxy Zoo 2: detailed morphological classifications for
304,122 galaxies from the Sloan Digital Sky Survey](https://arxiv.org/pdf/1308.3496v2.pdf)
- [SkyServer SQL Search](http://skyserver.sdss.org/dr13/en/tools/search/sql.aspx)
