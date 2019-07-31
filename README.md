# 8Meters
Website for 8 Meters Coworking

## Translations
https://docs.google.com/spreadsheets/d/1p7dc63aJllVhy6W6wqdp8z3oFY812EfYhce05Tl-eHo/edit

## AWS
### After making changes to the S3 bucket
Note that changes updated to the 8 meters bucket on S3 won't be seen on the site until AWS has updated the CloudFront cache.
To force an update, go the Cloud Front, click on the Distribution and select the Validations tab.
Create a new validation and type /*

This will take a minute to perform but will update the changes so they appear on the live website

### Caching
You should set the cache-control on items (such as images) so that they are cached on the users browser. If the user revisits the website, they will not need to re-download all the files again.

See the following article for further details:

https://stackoverflow.com/questions/10435334/set-cache-control-for-entire-s3-bucket-automatically-using-bucket-policies

## Announcement
If you wish to display the announcement in the first section, open the style.css file and search for 'announcement'.
Comment out the following line
```
display: none;
```
In .announcement:before, change the wording in the 'content' tag.

If you need the message to appear on a new line, use \A (or \A \A to leave a gap)

## Useful Info
Index_jp.html contains its own font-family Noto Sans JP within the style section

