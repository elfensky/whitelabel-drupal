# DEPENDENCIES FOR (HEADLESS) DRUPAL

by Andrei Lavrenov 2024

## DEFAULT DEPENDENCIES

these come preinstalled by default when you scaffold a new project with composer.

- composer/installers
- drupal/core-composer-scaffold
- drupal/core-project-message
- drupal/core-recommended

## TOOLING

- drush/drush -> a core tool that is used to manage drupal installation, configuration and databases
- drupal/symfony_mailer -> send emails from drupal, such as password resets etc.

#### only for non-headless drupal:

- drupal/twig_tweak -> additional twig functionality
- drupal/s3fs -> allows use of s3 buckets as a filesystem

## ADMINISTRATION

- drupal/gin -> modern administration theme with a sidebar
- drupal/gin_toolbar -> makes the sidebar visible in the frontend
- drupal/admin_toolbar -> extends the sidebar with a hover menu and extra features.

## CONTENT

- drupal/config_pages -> one-off custom content pages, like home, about, contact etc..

#### only for non-headless drupal:

- drupal/layout_paragraphs -> intuitive drag-and-drop experience for building flexible layouts with paragraphs.

## SEO/ANALYTICS

- drupal/metatag -> automatic metatags and opengraph tags for better SEO performance
- drupal/google_tag -> Google Analytics for the website
- drupal/pathauto -> pretty node links (/contentttype/title instead of /node/#)
- drupal/simple_sitemap -> automatically generate /sitemap.xml based on content

### NOT SURE ABOUT

- drupal/config_ignore -> sinds wij onze config exporteren/importeren bij deploy, mogen bepaalde zaken van config niet overschreven worden, zoals interface translations, custom blocks, etc...
  MAAR: download prod db, drush cex: al de nieuwe config is er nu bij.
  WAAROM dan nog nodig?

### STILL TO ADD

- drupal/entity_browser -> entity browser
- drupal/entity_browser_enhanced_form -> entity browser enhanced
  --> werkt samen met dropzonejs, toont een library van afbeeldingen of documenten

- drupal/dropzonejs -> media entity browser
- drupal/dropzonejs_eb_widget -> dropzonejs widget for entitybrowser
  --> zoek missch alternatief

- drupal/editor_advanced_link -> text editor allow target selection (target_blank enzo)
  --> dubbel check, if standard in CKE5 no longer needed

- drupal/focal_point -> image focal point for crop
  --> check if alternative exists. (no alternatives)

- drupal/menu_admin_per_menu -> gebruikers rollen naukeuriger/specifieker instellen.
  --> standaard is er geen rollen voor specifieke menu items, enkel "er aan of niet".
- drupal/role_delegation -> klant kan zelf rollen koppelen aan gebruikers, enkel rollen die niet hoger zijn dan die van hem.

- drupal/rebuild_cache_access -> klanten vragen om manueel cache te kunnen laten verversen.
  -> enkel installeren bij vraag

- drupal/webform -> webform module
- drupal/webform_ui -> webform ui module (zonder kan je enkel forms maken met xml)

- drupal/language_switcher_langcode -> language switcher bij block layout.

- drupal/inline_entity_form -> vanaf da ge werkt met entities (je hebt content types, je hebt taxonomies, content type heeeft detail, taxonomy niet. Entity is al de rest. config page is een entity.) -> gemakkelijkker ophalen en filteren.
  --> vooral met datums werken
