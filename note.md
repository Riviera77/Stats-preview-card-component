# Stats preview card component

Frontend | Stats preview card component

Le Pattern 7-1

Revenons à l'architecture. J'utilise habituellement ce que j'appelle le pattern 7-1: 7 dossiers, 1 fichier.
Tous vos partiels regroupés dans 7 dossiers différents et un fichier simple à la racine
(généralement appelé main. scss) qui les importe tous pour les compiler dans une feuille de style CSS.

• abstracts/
• base/
. components/
• layout/
• pages/
• themes/
• vendors/

Et bien sûr:
• main. scss

Exemple

sass/
|
|– abstracts/
| |– \_variables.scss # Sass Variables
| |– \_functions.scss # Sass Functions
| |– \_mixins.scss # Sass Mixins
| |– \_placeholders.scss # Sass Placeholders
|
|– base/
| |– \_reset.scss # Reset/normalize
| |– \_typography.scss # Typography rules
| … # Etc.
|
|– components/
| |– \_buttons.scss # Buttons
| |– \_carousel.scss # Carousel
| |– \_cover.scss # Cover
| |– \_dropdown.scss # Dropdown
| … # Etc.
|
|– layout/
| |– \_navigation.scss # Navigation
| |– \_grid.scss # Grid system
| |– \_header.scss # Header
| |– \_footer.scss # Footer
| |– \_sidebar.scss # Sidebar
| |– \_forms.scss # Forms
| … # Etc.
|
|– pages/
| |– \_home.scss # Home specific styles
| |– \_contact.scss # Contact specific styles
| … # Etc.
|
|– themes/
| |– \_theme.scss # Default theme
| |– \_admin.scss # Admin theme
| … # Etc.
|
|– vendors/
| |– \_bootstrap.scss # Bootstrap
| |– \_jquery-ui.scss # jQuery UI
| … # Etc.
|
`– main.scss # Main Sass file

Files should be imported according to the folder they live in, one after the other in the following order:

    abstracts/
    vendors/
    base/
    layout/
    components/
    pages/
    themes/

In order to preserve readability, the main file should respect these guidelines:

    one file per @import;
    one @import per line;
    no new line between two imports from the same folder;
    a new line after the last import from a folder;
    file extensions and leading underscores omitted.

@import 'abstracts/variables';
@import 'abstracts/functions';
@import 'abstracts/mixins';
@import 'abstracts/placeholders';

@import 'vendors/bootstrap';
@import 'vendors/jquery-ui';
