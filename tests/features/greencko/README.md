# Greencko Gherkin features

A list of features, and scenarios to have a full test over Greencko 8.x-6.x

If you want to run all Gherkin Features over a new Greencko site.
You will need to create the list of Testing users

## You can run the following command:
```
  $ bin/behat tests/features/greencko/ --format pretty --out std  --format html  --out reports/report-$( date '+%Y-%m-%d_%H-%M-%S' )
```

After that you can see the report in the ../behat/reports folder.

If you want to run the test in steps, if you are not interested in the
initialization and cleaning up after the test.

```
  $ ../../../private/bin/behat tests/features/greencko/step1-init-tests
  $ ../../../private/bin/behat tests/features/greencko/step2-apply-tests
  $ ../../../private/bin/behat tests/features/greencko/step3-cleanup-tests
```
For more custom commands: [Varbase Automated Functional Testing](https://github.com/metalbote/greencko/blob/master/tests/README.md)


## List of features in the step 1 init tests:
--------------------------------------------------------------------------------
* [Feature: Create default testing users.](https://github.com/metalbote/greencko/blob/master/tests/features/greencko/step1-init-tests/1-create-default-testing-users.feature)
```
webmaster: { email: 'webmaster@greencko.site', password: '.TZghbn56' }
test_authenticated: { email: 'authenticated.test@greencko.site', password: '.TZghbn56' }
test_editor: { email: 'editor.test@greencko.site', password: '.TZghbn56' }
test_content_admin: { email: 'content.admin.test@greencko.site', password: '.TZghbn56' }
test_seo_admin: { email: 'seo.admin.test@greencko.site', password: '.TZghbn56' }
test_site_admin: { email: 'site.admin.test@greencko.site', password: '.TZghbn56' }
test_super_admin: { email: 'super.admin.test@greencko.site', password: '.TZghbn56' }
```

## List of Features in the step 2 apply tests:
--------------------------------------------------------------------------------
* [01 - Feature: Website Base Requirements - User Registration - Only admins login](https://github.com/metalbote/greencko/blob/master/tests/features/greencko/step2-apply-tests/01-website-base-requirements/01-01-user-registration_only-admins-login.feature)

## List of features in the step 3 cleanup tests:
--------------------------------------------------------------------------------
* [Feature: Delete default testing users.](https://github.com/metalbote/greencko/blob/master/tests/features/greencko/step3-cleanup-tests/1-delete-default-testing-users.feature)
```
test_authenticated
test_editor
test_content_admin
test_seo_admin
test_site_admin
test_super_admin
```
