# List-of-Disposable-Email-Addresses
This is the list of up to dated email addresses.
Please notify me of any updates or fork and request a pull request if there is any updates available

### Gist
This is the link of the gist if you want to link to it and use it
[Disposable Email Addresses](https://gist.github.com/hassanazimi/d6e49469258d7d06f9f4 "Disposable Email Addresses")

### Pull Requests
Pull requests are welcome.

### Example of PHP usage:

If you want to avois users from registering with any disposable email addresses then you can use a function similar or exactly like this in `PHP`or your preferred programming language:

```php
function is_temp_mail($mail)
{
    $mail_domains_ko = file('https://gist.githubusercontent.com/hassanazimi/d6e49469258d7d06f9f4/raw/disposable_email_addresses');
    foreach($mail_domains_ko as $ko_mail) {
        [, $mail_domain] = explode('@', $mail);
        if(strcasecmp($mail_domain, trim($ko_mail)) == 0) {
            return true;
        }
    }
    return false;
}
```
