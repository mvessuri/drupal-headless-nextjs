# Next.js for Drupal

This is a Drupal site intended as a demo on how to work as a headless CMS to provide content to a Next.js application.

This is designed to be used in conjunction with the [Next.js for Drupal Demo](https://github.com/mvessuri/next-for-drupal) available on GitHub as a separate repository.

## Getting Started

To get started with this project, you'll need to have [Lando](https://lando.dev/) installed on your machine. Once you have Lando installed, you can start the project by running the following commands:

```bash
lando start
lando composer install
```

This will start the project and make it available at locally.

## Import Database

You can import a sample database using the following command:

`lando db-import dump.sql.gz`

## Connect to Next.js App

To connect your local instance of the Next.js app copy the following environment variables to your `.env.local` file:

```dotenv
# Required
NEXT_PUBLIC_DRUPAL_BASE_URL=http://next-for-drupal.lndo.site
NEXT_IMAGE_DOMAIN=next-for-drupal.lndo.site

# Required for On-demand Revalidation
DRUPAL_REVALIDATE_SECRET=secret

# Authentication (Bearer)
DRUPAL_CLIENT_ID=I-D3CFdgXdi4OGN5Do5hnm0v_n-eWKWJsx0bOdaFxKI
DRUPAL_CLIENT_SECRET=j19KG7oCbgmcvYXflqIp7mvp9t619Kgz


# Required for Preview Mode
DRUPAL_PREVIEW_SECRET=nextfordrupal
```


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.txt) file for details.
