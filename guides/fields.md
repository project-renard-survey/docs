# Fields

Fields allow you to save additional data about the elements, connections and loops in your map. Create whatever fields you need and modify the settings to enable things like checklists, prompts, currencies, and much more.

## Pre-named fields

Kumu comes with a few pre-named fields to get you started. Putting data in _all_ of these fields isn't necessary, but they get special visual treatment in [profiles](/guides/profiles.html), so it's great to use them when you can!

<dl>
    <dt>Label</dt>
    <dd>
      Use the Label field to give names to elements, connections, and loops. Your element and loop labels will appear on the map by default, and connection labels can be shown on the map as well, using the <code>label-visibility</code> <a href="/guides/property-reference.html">property</a> in the Advanced Editor.
    </dd>

    <dt>Type</dt>
    <dd>
      Use the type field to categorize elements and connections. Common element types include person, project, and company. Common connection types include personal, business, and family.
    </dd>

    <dt>Description</dt>
    <dd>
      The description field designed to hold longer-form content that describes an item. Descriptions can include multiple paragraphs, and even images and videos. <a href="/guides/markdown.html">You can use Markdown</a> to format each description's content.
    </dd>

    <dt>Tags</dt>
    <dd>
      The tags field is designed to hold multiple values that each describe your item in a different way. For example, a connection between a person and a non-profit might have "Strong relationship", "Board Member", "Donor", and "Advocate" all stored as separate values in the Tags field, adding rich detail to that person's relationship with the non-profit.
    </dd>

    <dt>Image</dt>
    <dd>
      Include an image URL and Kumu will display it on the map and in the profile.
    </dd>

    <dt>Email</dt>
    <dd>
      Add an email and Kumu will automatically include their <a href="http://en.gravatar.com/">gravatar</a> on the map and in the profile. Gravatars can be a huge time saver when working with social network data!
    </dd>

    <dt>ID</dt>
    <dd>
      Add a unique ID to each element and connection when you want to have fine-tuned control over Kumu's decision to create or update items during a <a href="/guides/import.html">spreadsheet import</a>. To learn more about this, check out <a href="/faq/how-do-I-avoid-duplicating-data.html">our guide on avoiding duplicate data</a>.
    </dd>
</dl>

## Add a field
To add a field, select an element or connection and then click the **+New Field** button in the sidebar. You'll be prompted to name the field and then enter a value for the element or connection you selected.

By default, new fields are set to accept only one value and not prompt users with suggested values. While this is an easy way to get started adding values, you may have times where you want people to pick from a list of defined values (level of influence: high, medium or low) or multiple values from a list (skills: project management, web development, leadership, public speaking). In those cases, you can customize your field—keep reading to learn how!

## Customize a field
To customize the settings for a given field, click on an element, and click the field in the element's profile.

![Customizing a field](/images/customize-field.gif)

A dropdown will appear with the following options:

- **Name** - change the name of your field
- **Type** - string, text, URL, email, number, currency
- **Limit** - one value **OR** none (one or more values)
- **Prompt** - none, autocomplete, or list
- **Category** - for grouping fields in sections on the profile
- **Visibility** - public **OR** private (whether or not viewers can see a given field)
- **Clustering** - whether to allow clustering by this field
- **More** - access settings, relevance, or delete the field

Let's look at a few of these options in more depth:

### Field type
Below are the choices for the field format and guidance on when to use each:

- **String** - This is the default value and used when entering simple, short pieces of text
- **Text** - Used for longer text fields like notes, addresses, and anywhere you want to use [Markdown](/guides/markdown.md) formatting
- **URL** - Used for website addresses
- **Email** - Used for email addresses
- **Number** - Used for numerical values that aren't currencies or dates
- **Currency** - Used for financial values to be displayed with standard currency format ($)
- **Date** - Used for dates, like February 14th (Kumu's birthday!)

### Field prompt
Field prompt is managed by clicking "more" and then "settings" in the dropdown. Below are the choices for the field prompt and guidance on when to use each:

- **None** - Use when you'd like to turn off any prompts for field values
- **Autocomplete** - Use when you'd like a tag-like interface for prompting values that match the current input
- **List** - Use when you want to pick from a list of defined values

### Field category
By default, all fields are ordered alphabetically based on the name of the field. You can also group fields by assigning them a category. For example, you may want to have all financial information (FY 2012 Investment, FY 2013 Investment and Cumulative Investment) under the category "Financials". You can create multiple categories and each will be ordered alphabetically.

We reserve a few category names that we give special treatment to:

- **General** - This is the default. Fields in this category will live at the top of the field section and won't have an explicit category label.
- **Footnotes** - This category is meant for things like attribution and citing your sources. Fields in this category will always be listed at the bottom of the profile.
- **Metrics** - This category holds any of the data you create using Kumu's [Metrics](/guides/metrics.md) tool.

## Field relevance
You can also manage field relevance through the project's settings to prevent irrelevant fields getting in the way of your work. Click the menu in the top left of your map and then click "fields". Scroll down and you'll see a "relevance" section. You can edit which fields should be included for each of the element and connection types in your project by clicking edit and unchecking the relevant fields.

![field relevance](/images/field-relevance.png)

By default, all fields are shown for all types. If you'd like to limit the fields that are shown, simply click edit and then uncheck the field you'd like to hide in the profile for a given type. Label, type, description, and tags are always shown for all types regardless of what you enter. Above is an example of customizing the profile of elements with type of "Company" to only show Image, Website, URL and Attribution.

## Field ordering
You can also use the field relevance menu to change the order fields are listed in the profile. By default all fields are listed alphabetically (and optionally broken into sections if you've assigned categories). The order of fields is unique to each element or connection type.

To change the order, click edit and then simply drag the fields to reorder them. When you are finished, click "Done" and you'll see the new order reflected in the profile.

## Deleting a field
If you've created a field and want to delete it and all corresponding values, click on the label of the field in any profile and then go to more -> delete. Alternatively, use can use the menu in the upper left corner to go to the field settings page (choose fields). This will delete the field and any values assigned for any content in your project.

## Deleting field values
Occasionally you may want to delete the prompted choices for a given field, or the options that show up in your legend or in a [control](/guides/controls.md). To do this, you need to delete the underlying field value. This process is different, depending on the field's [prompt](#customize-a-field).

For fields that have their prompt set to "Autocomplete" or "None" (this includes the Tags field), you can only delete the field value by removing it from every element, connection, and loop in the project, including the [trash](/overview/kumus-architecture.html#trash).

For all other fields, follow these steps:
1. Click the menu in the upper left of your map and choose **FIELDS**
1. Click on the field you want to edit
1. Find the value you want to delete. Then, highlight it and press `delete` or `backspace` on your keyboard.
1. Scroll down and click **SAVE** to save your changes

After you follow these steps and refresh the page, the field value(s) you deleted will no longer show up in prompted lists or in controls.


<span class="edit-link"><a href="https://github.com/kumu/docs/blob/master/guides/fields.md" target="_blank"><i class="fa fa-github"></i> edit this page</a></span>
