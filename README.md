# Meta Conversions API Tag for Google Tag Manager (Server-side)
The Meta Conversions API Tag is a Server-to-Server (S2S) integration that allows you to share website and app visitor events directly to the graph api. Data that is shared via the Conversions API is processed similar to information shared via other face data integration business tools, like the Meta pixel.

This Tag uses the standard GA4 Client and parses GA4 input into Meta data and sends it through the Conversions API.

If a sub domain is set up and the pixel is not being used, the script will generate  and store cookie values for *fbp* and *fbc* when possible.

This tag will try to match as many parameters as possible from the GA4 client request to the Meta Conversions API.

If you are using other user data parameters  than the GA4 standard then you can manually change to those in this tag.  You have the possibility to manually match parameters.

/This tag also supports to send from other sources/

## Current Version
This tag currently runs Graph API Version **v14.0**

## Input variables
* Meta Pixel ID
* Meta Conversions API Token 
* (optional) Test Event Code

## GA4 Standard Events Mapping
The Tag parses all GA4 Client Events into Meta Events. 

### Mapped Events (GA4 => Meta)

  `add_payment_info - AddPaymentInfo`
  `add_to_cart - AddToCart`
  `add_to_wishlist - AddToWishlist`
  `complete_registration - CompleteRegistration`
  `contact - Contact`
  `customize_product - CustomizeProduct`
  `donate - Donate`
  `find_location - FindLocation`
  `begin_checkout - InitiateCheckout`
  `generate_lead - Lead`
  `page_view - PageView`
  `purchase - Purchase`
  `schedule - Schedule`
  `search - Search`
  `start_trial - StartTrial`
  `submit_application - SubmitApplication`
  `subscribe - Subscribe`
  `view_item - ViewContent`

*Note: /Some of the events above are not GA4 standard events but are added to simplify the setup/*

## Other ways to use the Tag
If you are not using GA4 standard events you can still use this tag to send data to Meta.

The request Parameters supported are

/*Server Event Data*/

`x-fb-event-name` - Event Name
`x-fb-event-time` - Timestamp in seconds
`x-fb-event-source-url` - Url for where the event appeared.
`x-fb-event-id` - Event ID used for deduplication
`x-fb-action-source` - Action source (default: website)
`x-fb-opt-out` - Boolean - user opt out
`x-fb-data-processing-options` - Data processing options
`x-fb-data-processiong-options-country` - Data processing options country
`x-fb-data-processing-options-state` - Data processing options state

/*Custom Data*/ 

`x-fb-content-category` - String -  Content category
`x-fb-content-ids` - Array - Content Ids
`x-fb-content-name` - String - Content name
`x-fb-contents` -  Array of objects - Contents 
`x-fb-currency` - String - currency
`x-fb-delivery-category` - String - delivery category
`x-fb-num-items` - String - num items
`x-fb-order-id` - String - order id
`x-fb-predicted-ltv` - Float - predicted itv
`x-fb-search-string` - String - search string
`x-fb-status` - string - status
`x-fb-value` - float - Value


/*User Data*/

`x-fb-email` 
`x-fb-phone-number`  
`x-fb-first-name` 
`x-fb-last-name`
`x-fb-city`
`x-fb-state`
`x-fb-zip-code` 
`x-fb-country`    
`x-fb-external-id`
`x-fb-subscription-id` 
`x-fb-lead-id`
`x-fb-fbp`
`x-fb-fbc`    
`x-fb-client-ip-address`
`x-fb-client-user-agent`  

## Links
[_Meta Conversions API_](https://ads.tiktok.com/marketing_api/docs?id=1701890979375106)

[_Google Tag Manager Server Side_](https://developers.google.com/tag-platform/tag-manager/server-side)

[_GA4 Send Data_](https://developers.google.com/tag-platform/tag-manager/server-side/send-data)

