# Quickbooks Online Integration

## Overview

[Quickbooks](http://quickbooks.intuit.com) is an accounting software package developed and marketed by [Intuit](http://www.intuit.com). This implementation uses the [Quickbooks v3 API](https://developer.intuit.com/apiexplorer?apiname=V3QBO) through the [quickbooks-ruby](https://github.com/ruckus/quickbooks-ruby) gem.

Please visit the [wiki](https://github.com/flowlink/quickbooks_integration/wiki) for further info on how to connect this integration, but here's a quick tip:

This is a fully hosted and supported integration for use with [FlowLink](http://flowlink.io). With this integration you can perform the following functions:

* Send orders to Quickbooks as Sales Receipts
* Send products to Quickbooks as Items
* Send returns to Quickbooks as Credit Memo
* Poll for inventory stock levels in Quickbooks

[FlowLink](http://flowlink.io) allows you to connect to your own custom integrations.
Feel free to modify the source code and host your own version of the integration
or better yet, help to make the official integration better by submitting a pull request!

![Wombat Logo](http://spreecommerce.com/images/wombat_logo.png)

This integration is 100% open source an licensed under the terms of the New BSD License.

### 21 Character limit on Order numbers.

If your having problems with it, this transform should help:
```javascript
//nomustache
payload.order.number = payload.order.number.substring(0, 21);
```
