# ga4-datalayers 
This repository has the purpose to serve as guidance for implementing e-commerce tracking by using datalayers. 

## Reason

As analysts we need to gather as much information as possible from the tools available to answer key questions that may arise over time. There are many tools like GA4, Hotjar, Microsoft Clarity, among others, that answer questions like:

☑️ What is happening?

☑️ Where it is happening?

☑️ When it happened?


However, the **"Why"** is the target we aim to answer. Therefore, it is fundamental to collect as much information as possible. In marketing, the information collected is used by advertising platforms  to create remarketing campaigns, predict the probabilities of a user converting, and estimating costs. 

## What could you find here

The repository will list a simple e-commerce datalayer setup I implemented in my [blog](juanferespinosa.com/blog/ecommerce/products), where you could find a step-by-step guide.

As a summary, according to [Google documentation](https://developers.google.com/analytics/devguides/collection/ga4/ecommerce?client_type=gtag) there are several default event names for tracking information in e-commerce.  

> [!TIP]
> It is a good practice to use Google´s default event names as it will automatically populate standard reports.
>
> Always use the events with underscores.

The next step is to be clear the purpose of each event, define the information you want to collect, modify the following datalayers with your custom examples, ask your developer to implement, and finally test them with Google Tag Manager.


In my example, here is how I defined the event sequence of the ecommerce section.

1. A user views in the product list of a category and view them.                        ➡️ **Event:**  [_view_item_list_](https://gist.github.com/juanferEspinosa/2a402392488fe40801c83d6fe627df9a)
2. A user clicks a particular product to read more information about it.                   ➡️ **Event:** [_select_item_](https://gist.github.com/0c83381d1ffad4bb2834a4ad6706e567.git)
3. A user sees an individual product page.                                                 ➡️ **Event:** [_view_item_](https://gist.github.com/303dce1fc718b95154eeed40aece62d5.git)
4. A user add the product to cart.                                                         ➡️ **Event:** [_add_to_cart_](https://gist.github.com/juanferEspinosa/1df6975389bac25faf22c7957d6ecb47)
5. A user can also remove a product from the cart.                                         ➡️ **Event:** [_remove_from_cart_](https://gist.github.com/juanferEspinosa/c4eeea6ec935105f9821f11ef3123d1f)
6. A user views the cart page.                                                             ➡️ **Event:** [_view_cart_](https://gist.github.com/juanferEspinosa/1643614ba7f9b6d7116371dd80a41810)
7. A user initializes the checkout.                                                        ➡️ **Event:** [_begin_checkout_](https://gist.github.com/juanferEspinosa/f3e631afacce28a94c967fc4d246413f)
8. A user adds billing and/or shipping information.                                        ➡️ **Event:** [_add_shipping_info_](https://gist.github.com/juanferEspinosa/9746b90b4df8e87a1736aa28050e0bd1), [_add_payment_info_](https://gist.github.com/juanferEspinosa/f10da32ffb1fc0d1bd5562f804b4b328)
9. A user completes the purchase                                                          ➡️ **Event:** [_purchase_](https://gist.github.com/juanferEspinosa/7cb20d976fb9706958fa39b6ea6915fb)

> [!NOTE]
> The order of the events, _Shipping information_ and _billing information_ does not matter as Google will understand them.
>
> For a deeper understanding of events and the parameters that can be added to an individual event throughout the purchase funnel, refer to [Simo Ahava's post](https://www.simoahava.com/analytics/google-analytics-4-ecommerce-guide-google-tag-manager/). 


   
 
