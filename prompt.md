1/ Translation Instructions
Translate all user-facing text and content in full, without skipping, omitting, or leaving any text untranslated, regardless of its formatting or presentation. This includes:
- Bold or emphasized text: Translate all bold, italicized, or otherwise formatted text.
- Text in quotation marks: Translate all text enclosed in double quotation marks ("...") or single quotation marks ('...').
- In-app content and UI labels: Translate all button names, menu items, tab names, settings, navigation labels, notifications, and other in-app text, even when they appear within quotation marks or are formatted in bold.
- Examples and instructions: Translate UI text referenced in explanations, examples, step-by-step instructions, and documentation.
- Bold text that is in-app content or a button: When bold text refers to content or a button that appears in the app, follow the current localization in the app for the target language. Use the in-app string exactly as it appears in the app, and do not create your own translation. Use the in-app strings provided with this request (localization file or glossary) as the source. If an in-app string is not provided or cannot be found, translate it yourself and list it under "Needs verification" at the end.
Important: Formatting and quotation marks do not indicate that text should be preserved in its original language. Always translate the text inside them while retaining the original formatting and quotation marks where appropriate. The current in-app localization always takes priority over your own translation.

2/ UI Label Detection and Localization Sources
Treat text as a possible in-app UI label when it appears in bold, quotation marks, a breadcrumb or navigation path, a component title, or after an action verb such as "tap", "click", "select", "choose", "open", "go to", "navigate to", "switch", or "toggle". This includes buttons, tabs, menus, settings, section names, statuses, notifications, and dialog actions.

Determine the platform of each instruction before looking up a label. Do not reuse an iOS translation for Android, or an Android translation for iOS, unless the official resources use the same value.

Use these sources of truth:

- Documentation source and locale files: `/Users/manhbui/Works/Habitify/habitify-public-docs`
- iOS, iPadOS, watchOS, widgets, Shortcuts, and other Apple-platform localization catalogs: `/Users/manhbui/Downloads/habitify-localization`
- Android localization resources: `/Users/manhbui/Works/Habitify/habitify-android/app/src/main/res`

For Apple-platform labels, search all relevant `.xcstrings` catalogs. Match the English source string and use the target locale value from the catalog that belongs to the feature being documented.

For Android labels, first locate the English string and its resource key in `values/`, then use the value with the same resource key from the target locale directory, such as `values-ja/` or `values-es/`. Include feature-specific resources such as `habit_gate.xml`; do not search only the main locale file.

When one English label has multiple translations, choose by platform, feature, resource key, and surrounding UI context. Do not choose a translation solely because its English source text matches. Distinguish Habitify UI labels from operating-system labels such as the iOS or Android Settings app.

The non-translatable product-name list below overrides localization catalogs. If no authoritative label can be found, translate it naturally and add an entry under `Needs verification` containing the file, platform, English source label, proposed translation, and paths searched.

3/ Terms That Must Not Be Translated
Keep the following third-party app, service, and product names exactly as written:
- Apple Health
- Health Connect
- Strava
- Fitbit
- RescueTime
- Apple Calendar
- Google Calendar
- Outlook Calendar
- Zapier
- IFTTT
Do not translate, localize, or modify these brand and product names.
4/ Final Quality Check
Before completing the translation:
1. Ensure that every piece of user-facing source text has been translated.
2. Verify that no bold text, quoted text, button names, or in-app UI labels have been accidentally skipped.
3. Verify that every bold in-app label or button follows the current in-app localization, or is listed under "Needs verification".
4. Preserve the original document's structure, formatting, and meaning.
5. Keep all specified third-party product and service names unchanged.
6. Verify each detected UI label against the platform-specific source above. Do not report completion while `Needs verification` items remain unreported.
Completeness is mandatory: No text should be skipped simply because it is bold, quoted, or represents an in-app UI element.
