.. _how_to_guides__configuring_metadata_stores__how_to_configure_an_expectation_store_in_git:

How to configure an Expectation store in git
============================================

We recommend that you use GIT version control to keep track of expectations.

.. admonition:: Prerequisites: This how-to guide assumes that you have already:

    - Configured a Data Context
    - Configured an Expectation Suite
    - Configured and linked your ``great_expectations`` folder to a git repository


Once the files have been uploaded to the Git-branch, you can observe the history of expectations and how they have changed by typing
``git log -p npi_expectations``.

Notice the informative messages you get when you


.. code-block:: bash

    commit cbc127fb27095364c3c1fcbf6e7f078369b07455
    Author: William Shin <will@superconductive.com>
    Date:   Tue Jun 2 16:24:18 2020 -0700

        adjusting expectations in branch

    diff --git a/great_expectations/expectations/npi_expectations.json b/great_expectations/expectations/npi_expectations.json
    index d1dc0ef..083ff0c 100644
    --- a/great_expectations/expectations/npi_expectations.json
    +++ b/great_expectations/expectations/npi_expectations.json
    @@ -17,7 +17,7 @@
         {
           "expectation_type": "expect_table_column_count_to_equal",
           "kwargs": {
    -        "value": 333
    +        "value": 331
           },
           "meta": {
             "BasicSuiteBuilderProfiler": {

    commit 05b3c8c1ed35d183bac1717d4877fe13bc574963
    Author: William Shin <will@superconductive.com>
    Date:   Tue Jun 2 16:23:02 2020 -0700

        changed expectations

    diff --git a/great_expectations/expectations/npi_expectations.json b/great_expectations/expectations/npi_expectations.json
    index a75a0aa..d1dc0ef 100644
    --- a/great_expectations/expectations/npi_expectations.json
    +++ b/great_expectations/expectations/npi_expectations.json
    @@ -17,7 +17,7 @@
         {
           "expectation_type": "expect_table_column_count_to_equal",
           "kwargs": {
    -        "value": 330
    +        "value": 333
           },
           "meta": {
             "BasicSuiteBuilderProfiler": {
    @@ -1573,4 +1573,4 @@
           "format": "markdown"
         }
       }
    -}
    \ No newline at end of file
    +}



.. discourse::
    :topic_identifier: 181
