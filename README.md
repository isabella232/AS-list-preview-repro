1. [`@layout/plain_listview`](/app/src/main/res/layout/plain_listview.xml):
 
  References plain `ListView`, with no `tools:` attributes.
  * **Expected**: Shows a list of _"Item N"_ / _"Sub Item N"_ list items.
  * **Actual**: :+1: Correct

    ![](/screenshots/plain-listview.png)
   
2. [`@layout/plain_listview_custom_listitem`](/app/src/main/res/layout/plain_listview_custom_listitem.xml)

  References plain `ListView`, with `tools:listitem` and `tools:listheader`
    attributes (pointing to [`@layout/preview_item`](/app/src/main/res/layout/preview_item.xml))
  * **Expected**: Shows a list of "Item N" / "Sub item N" list items, with
    colored backgrounds behind the text.
  * **Actual**: :-1: Shows same preview as #1: 
 
    ![](/screenshots/plain-listview-custom-listitem.png)

3. [`@layout/subclass_listview`](/app/src/main/res/layout/subclass_listview.xml)

  References a subclass of `ListView`, with `tools:listitem` and
    `tools:listheader` attributes (pointing to
    [`@layout/preview_item`](/app/src/main/res/layout/preview_item.xml))
  * **Expected**: Shows a list of "Item N" / "Sub item N" list items, with
    colored backgrounds behind the text (as expected for #2)
  * **Actual**: :-1: Shows a blank preview, as if it is an empty `ViewGroup`: 

    ![](/screenshots/subclass-listview.png)