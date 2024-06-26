.. _valueSelectsV2:

Value selects
=============

.. seealso:: :ref:`UX guidelines on value selects <uxValueSelect>`

.. toctree::
  :hidden:

  value-select/globalValueSelect

Value selects allow you to create a **drop-down menu of textual options** for the user to select from instead of entering a number.
 
This is great for specifying **common presets for a variable**, or to create switches that turn calculator features on and off.

How to define a value select
----------------------------

In Engine v2, there are 2 ways to define a value select:

* Create a value select specific to the calculator from scratch; or
* Import from a :ref:`Global Value Select<globalValueSelectsV2>` to store a **local copy** of it within the calculator.

Creating a value select
-----------------------

In Engine v2, you can create 2 different kinds of value selects:

* Simple value select; and
* Multi-level value select (documentation coming soon), of which there are two types:

   * Multi-level single value select; and
   * Multi-level split value select.

Simple value select
^^^^^^^^^^^^^^^^^^^

In the **Value selects** section of the edit calculator page, here are the steps to create a value select:

1. Click the **Add first value select** button to start creating a new value select.

.. figure:: img/simple-VS-step1.png
  :align: center

2. Give your new value select a descriptive name. It will be used in the variable attribute **Value select**.
3. Enter a name for the first item of the value select. This name is what the **user sees in the drop-down menu**, so make sure it will make sense to the user.

.. figure:: img/simple-VS-step3.png
  :align: center

4. Next, **enter a value** to associate with this first option. The variable that uses this value select will take this value when this option is selected by the user.

.. figure:: img/simple-VS-step4.png
  :align: center

5. Go ahead and add other value select items. **Press the plus icon** (“Add a sibling”) to add another one.

.. figure:: img/simple-VS-step5.png
  :align: center

6. Continue adding all options...

.. figure:: img/simple-VS-step6.png
  :align: center

.. _valueSelectsV2TieToVariable:

7. Finally, associate a variable with this value select by setting the variable type to **Value select** in the variable attributes.

.. figure:: img/simple-VS-step7.png
  :align: center

8. Then choose the name of the value select you created in the **Value select name** field, to tie it to the variable.

.. figure:: img/simple-VS-step8.png
  :align: center


By selecting an option from the drop-down list, the variable takes the value defined in value select. So the variable can still be used in equations as usual.

Additional options in value select
""""""""""""""""""""""""""""""""""

You may configure the value select in different ways depending on your need. The available options are:

1. **Value select type**: The value select type can be any of the following:

.. _valueSelectsV2DropdownOption:

   a. **Dropdown** — recommended when there are more than 5 options. Using this will display your choices as a dropdown menu from which the user can select their required option. Read more about its UX guidelines :ref:`here <uxDropdown>`.

      .. figure:: img/vs-dropdown.png
       :alt: example of a dropdown list value select
       :width: 50%
       :align: center

      (You may also feel free to use the dropdown option for **5 or fewer** options as you see fit.)

.. _valueSelectsV2RadioButtonOption:

   b. **Radio button** — recommended when there are **5 or fewer options**. Using this will display all choices as radio buttons from which the user can choose one. With this type, the user will be able to **see all options right away** without requiring them to click the dropdown. Read more about its UX guidelines :ref:`here <uxRadioButtons>`.

      .. figure:: img/vs-radio.png
       :alt: example of a radio list value select
       :width: 50%
       :align: center

      .. note::
        1. You will **not** be able to use this option when there are **more than 5 options**.
        2. You will have to **set a default value** for the variable when using the radio button option.

.. _valueSelectsV2CheckboxOption:

   c. **Checkbox** — If there are only 1 or 2 options, you can select the Checkbox type. Read more about its UX guidelines :ref:`here <uxCheckbox>`.

      .. figure:: img/checkbox-example.png
       :alt: example of a checkbox value select
       :width: 50%
       :align: center

      **Use case for “Checkbox” in a Value select with 1 option:**
      
      The option's value represents the value of the connected variable in the “checked” state. The unchecked state is by default associated with a NULL value.

      **So use value select checkbox with a single option only if you “want” the unchecked state to be NULL.**

      .. figure:: img/checkbox-1-option.png
        :alt: example of a checkbox with 1 option
        :width: 95%
        :align: center

        ؜

      .. note::
        If you don't set a default value for the variable it will have a value of **null** on initial loading of the calculator.

      **Use case for “Checkbox” in a Value select with 2 options:**

      If you need the unchecked state to be a different value such as 0, we need a value select with 2 options. The **first option's value** represents the variable's value in **“checked”** state. The **second option's value** represents the variable's value in **“unchecked”** state.

      Use this option when you want the variable to be included in calculations even in unchecked state, by giving the “unchecked” state a value.

      .. figure:: img/checkbox-2-option.png
        :alt: example of a checkbox with 2 option
        :width: 95%
        :align: center

        ؜

      For instructions on how to create a checkbox, see :ref:`Checkbox value select<valueSelectsV2Checkbox>` below.

1. **Optional additional columns**: You may configure additional columns to hold additional data about each choice. For example, if you are listing car models, you could use additional columns to configure each model's mileage, color, etc. *More about this option at a later date in the value setter section.*

.. figure:: img/vs-optional-columns.png
       :alt: example of optional columns in a value select
       :width: 95%
       :align: center

|

.. _valueSelectsV2Checkbox:

Checkbox value select
^^^^^^^^^^^^^^^^^^^^^

To create a checkbox type variable, we first need to **create a value select of type checkbox**. A value select with one or two options is configurable as a checkbox.

1. Create the value select checkbox by clicking "Add first value select".

.. figure:: img/checkbox-step1.png
  :align: center

  ؜

2. Configure the value select with **only one** option.

.. figure:: img/checkbox-step2.png
  :align: center

  ؜

3. The value of the option will represent the value of the connected variable in the **"checked" state**.

.. figure:: img/checkbox-step3.png
  :align: center

  ؜

4. From the "Type" dropdown, choose **"checkbox"**. This option will show up **only if** the value select has 1 or 2 values.

.. figure:: img/checkbox-step4.png
  :align: center

  ؜

5. Click on the variable that should be tied to the value select checkbox.

.. figure:: img/checkbox-step5.png
  :align: center

  ؜

6. Choose "Value select" option in the "Variable type" attribute.

.. figure:: img/checkbox-step6.png
  :align: center

  ؜

7. Choose the value select checkbox that was created.

.. figure:: img/checkbox-step7.png
  :align: center

  ؜

8. Reload the calculator preview and now the variable will show up as a checkbox in the calculator panel.

.. figure:: img/checkbox-step8.png
  :align: center

  ؜

9. Checking the checkbox will set the value of the variable to the one configured in the value select.

.. figure:: img/checkbox-step9.png
  :align: center

  ؜

.. tip::
  You can either use the variable label to specify what checking a box means or the value select option name. The latter is nice to make a list of checkboxes by removing the label for each variable. Read more about this use-case in the :ref:`UX guidelines <uxDropdown>`.

  .. figure:: img/checkbox-tip.png
    :align: center

    ؜
