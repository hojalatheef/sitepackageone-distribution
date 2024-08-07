# SitePackageOne Distribution

SitePackageOne is a TYPO3 site package designed for a one-page website. This
package provides the necessary templates, TypoScript configuration, and content
elements to quickly set up a modern, responsive one-page site using TYPO3
version 13.

## Requirements

- TYPO3 v13
- PHP 8.2 or higher
- MySQL 5.7+ or MariaDB 10.4+
- Web server (Apache, Nginx)

## Installation

### 1. Set Up TYPO3 Environment

#### Prerequisites:

- Ensure your web server, PHP, and database are correctly set up and configured.

Clone the `sitepackageone` repository to your local machine.

```sh
git clone git@github.com:hojalatheef/sitepackageone-distribution.git
cd sitepackageone-distribution
```

### 2. Start DDEV

Ensure you have DDEV installed on your system. If not, follow the DDEV
installation guide.

Start the DDEV environment:

```sh
ddev start
```

### 3. Install Dependencies

```sh
ddev composer install
```

### 4. Customize Your One-Page Template

1. **Create Content Elements**:
    - Go to "WEB" > "Page".
    - Create and configure content elements on your root page using the provided
      templates.

2. **Edit HTML Templates**:
    - The HTML templates are located
      in `Source/Extension/sitepackageone/Resources/Private/Templates`.
    - Customize these templates to fit your design needs.

### 5. Add Custom Styles and Scripts

1. **CSS and JS Files**:
    - Add your custom CSS files
      to `Source/Extension/sitepackageone/Resources/Public/Css`.
    - Add your custom JavaScript files
      to `Source/Extension/sitepackageone/Resources/Public/JavaScript`.

2. **Include Custom Styles and Scripts in TypoScript**:
    - Open the TypoScript setup file located
      at `Source/Extension/sitepackageone/Configuration/TypoScript/setup.typoscript`.
    - Include your custom styles and scripts as needed:

   ```typoscript
   page.includeCSS {
       file1 = EXT:sitepackageone/Resources/Public/Css/styles.css
   }

   page.includeJSFooter {
       file1 = EXT:sitepackageone/Resources/Public/JavaScript/scripts.js
   }
   ```

## Contributing

We welcome contributions to improve SitePackageOne. Please submit issues and
pull requests on
the [GitHub repository](https://github.com/yourusername/sitepackageone).

## License

SitePackageOne is released under the MIT License. See the [LICENSE](LICENSE)
file for more details.
