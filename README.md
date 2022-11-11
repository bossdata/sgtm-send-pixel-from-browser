# sgtm-send-pixel-from-browser
Send pixel from browser - Custom Tag Template (Server) for Google Tag Manager.

This template is usefull when there is no server side tag available (yet) for your provider or that it is not fully implemented. It was inspired by the fact that the current server side tags for DV360 Floodlight do not support all available variables in the tag, for example we needed to set match_id so we coan assign conversions to the web user through the DV360 Conversion API.

With this template you can use the static img tags for any provider that supplies them and fire them in the browser from server gtm triggers, much like you would in a web gtm container. You will  have the benefit of your standarised SERVER GTM (e.g. from GA4) without having to maintain and mimic the same tags and triggers in WEB GTM.

This tag allows you to re-recreate the src url for your img pixel and add a query string from gtm variables in the requested format, here are some examples of IMG tags for frequently used providers: 

| PROVIDER                                                                                    | IMG PIXEL URL                            | QUERY STRING SEPARATOR | VARIABLE SEPARATOR | VALUE SEPARATOR |
|:--------------------------------------------------------------------------------------------|------------------------------------------|:----------------------:|:------------------:|:---------------:|
| [BING IMG TAG](https://help.ads.microsoft.com/apex/index/3/en/60122)                        | https://bat.bing.com/action/0            |           ?            |         &          |        =        |
| [DV360 FLOODLIGHT IMG TAG](https://support.google.com/campaignmanager/answer/2823450?hl=en) | https://ad.doubleclick.net/ddm/activity/ |                        |         ;          |        =        |

