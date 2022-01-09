# WordPress GitHub Plugin Updater
Updates a WordPress plugin from GitHub private repository.

## Usage
Simply adds this lines to your main plugin file:

```
if (is_admin()) {
    define('GH_REQUEST_URI', 'https://api.github.com/repos/%s/%s/releases');
    define('GHPU_USERNAME', 'YOUR_GITHUB_USERNAME');
    define('GHPU_REPOSITORY', 'YOUR_GITHUB_REPOSITORY_NAME');
    define('GHPU_AUTH_TOKEN', 'YOUR_GITHUB_ACCESS_TOKEN');

    include_once plugin_dir_path(__FILE__) . '/GhPluginUpdater.php';

    $updater = new GhPluginUpdater(__FILE__);
    $updater->init();
}
```

* Sets your GitHub user name in GHPU_USERNAME constant.
* Sets your GitHub repository name in GHPU_REPOSITORY constant.
* Sets your GitHub token in GHPU_AUTH_TOKEN constant. You can get this in Your Account => Settings => Developer Settings => Personal access tokens => Generate new token.
* Includes GhPluginUpdater class

## Additional information
You have more information (in Spanish) on my [blog](https://desarrollowp.com/blog/tutoriales/como-actualizar-un-plugin-de-wordpress-desde-un-repositorio-privado-de-github/).

If you have any comment, suggestion or similar, plese use discussions or pull requests.
