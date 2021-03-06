.. _api:

=============
API Reference
=============

This page lists all of the estimators and top-level functions in ``dask_ml``.
Unless otherwise noted, the estimators implemented in ``dask-ml`` are
appropriate for parallel and distributed training.

:mod:`dask_ml.model_selection`: Model Selection
===============================================

.. automodule:: dask_ml.model_selection
   :no-members:
   :no-inherited-members:

.. currentmodule:: dask_ml

Dask-ML has a few cross validation utilities.

.. autosummary::
   :toctree: generated/

   model_selection.train_test_split

:func:`model_selection.train_test_split` is a simple helper that
uses :class:`model_selection.ShuffleSplit` internally.

.. autosummary::
   :toctree: generated
   :template: class.rst

   model_selection.ShuffleSplit

Dask-ML provides drop-in replacements for grid and randomized search.

.. autosummary::
   :toctree: generated/
   :template: class.rst

   model_selection.GridSearchCV
   model_selection.RandomizedSearchCV


:mod:`dask_ml.linear_model`: Generalized Linear Models
======================================================

.. automodule:: dask_ml.linear_model
   :no-members:
   :no-inherited-members:

.. currentmodule:: dask_ml

.. autosummary::
   :toctree: generated/
   :template: class.rst

   linear_model.LinearRegression
   linear_model.LogisticRegression
   linear_model.PoissonRegression

Meta-estimators for scikit-learn
================================

dask-ml provides some meta-estimators parallelize certain components.

.. currentmodule:: dask_ml

.. autosummary::
   :toctree: generated/
   :template: class.rst

   wrappers.ParallelPostFit


Incremental Learning
====================

.. currentmodule:: dask_ml

Some scikit-learn estimators support out-of-core training through the
``partial_fit`` method. The following estimators wrap those scikit-learn
estimators, allowing them to be used in Pipelines and on Dask arrays and
dataframes. Training will still be serial, so these will not benefit from
a parallel or distributed training any more than the underlying estimator.

.. autosummary::
   :toctree: generated/
   :template: class.rst

   cluster.PartialMiniBatchKMeans
   linear_model.PartialPassiveAggressiveClassifier
   linear_model.PartialPassiveAggressiveRegressor
   linear_model.PartialPerceptron
   linear_model.PartialSGDClassifier
   linear_model.PartialSGDRegressor
   naive_bayes.PartialBernoulliNB
   naive_bayes.PartialMultinomialNB


:mod:`dask_ml.cluster`: Clustering
==================================

.. automodule:: dask_ml.cluster
   :no-members:
   :no-inherited-members:

.. currentmodule:: dask_ml

.. autosummary::
   :toctree: generated/
   :template: class.rst

   cluster.KMeans
   cluster.SpectralClustering


:mod:`dask_ml.decomposition`: Matrix Decomposition
====================================================

.. automodule:: dask_ml.decomposition
   :no-members:
   :no-inherited-members:

.. currentmodule:: dask_ml

.. autosummary::
   :toctree: generated/
   :template: class.rst

   decomposition.PCA
   decomposition.TruncatedSVD


:mod:`dask_ml.preprocessing`: Preprocessing Data
================================================

.. automodule:: dask_ml.preprocessing

.. currentmodule:: dask_ml

.. autosummary::
   :toctree: generated/
   :template: class.rst

   preprocessing.StandardScaler
   preprocessing.RobustScaler
   preprocessing.MinMaxScaler
   preprocessing.QuantileTransformer
   preprocessing.Categorizer
   preprocessing.DummyEncoder
   preprocessing.OrdinalEncoder


:mod:`dask_ml.metrics`: Metrics
===============================

Score functions, performance metrics, and pairwise distance computations.

Regression Metrics
------------------

.. currentmodule:: dask_ml

.. autosummary::
   :toctree: generated/

   metrics.mean_absolute_error
   metrics.mean_squared_error


Classification Metrics
----------------------

.. currentmodule:: dask_ml

.. autosummary::
   :toctree: generated/

   metrics.accuracy_score


:mod:`dask_ml.tensorflow`: Tensorflow
=====================================

.. automodule:: dask_ml.tensorflow

.. currentmodule:: dask_ml.tensorflow

.. autosummary::
   :toctree: generated/

   start_tensorflow



:mod:`dask_ml.xgboost`: XGBoost
===============================

.. automodule:: dask_ml.xgboost

.. currentmodule:: dask_ml.xgboost

.. autosummary::
   :toctree: generated/
   :template: class.rst

   XGBClassifier
   XGBRegressor

.. autosummary::
   :toctree: generated/

   train
   predict
