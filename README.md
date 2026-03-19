# NoPayn Payment Gateway for OpenCart 4

Accept payments via [NoPayn/Cost+](https://costplus.io) in your OpenCart 4 store.

## Supported Payment Methods

- **Credit / Debit Card** — Visa, Mastercard, Amex, Maestro, V Pay, Bancontact, Diners, Discover
- **Apple Pay**
- **Google Pay**
- **Vipps / MobilePay**

## Requirements

- OpenCart 4.0.0.0 or later
- PHP 8.0 or later
- A NoPayn merchant account ([sign up](https://manage.nopayn.io/))

## Installation

### Method A: Upload via Admin Panel

1. Download the latest release `.ocmod.zip` from [Releases](https://github.com/NoPayn/nopayn-opencart/releases)
2. In your OpenCart admin, go to **Extensions → Installer**
3. Upload the `.ocmod.zip` file
4. Go to **Extensions → Extensions → Payment**
5. Find **NoPayn Payment Gateway** and click **Install**, then **Edit**

### Method B: Manual Upload

1. Download or clone this repository
2. Copy the contents of `upload/` into your OpenCart root directory
3. Go to **Extensions → Extensions → Payment**
4. Find **NoPayn Payment Gateway** and click **Install**, then **Edit**

## Configuration

1. Enter your **API Key** (found in the [NoPayn merchant portal](https://manage.nopayn.io/) under Settings → API Key)
2. Enable the **payment methods** you have been approved for
3. Set your preferred **order statuses** for completed, pending, and cancelled payments
4. Optionally restrict by **Geo Zone**
5. Set **Status** to enabled
6. Save

## How It Works

This extension uses the NoPayn **Hosted Payment Page (HPP)** flow:

1. Customer selects a NoPayn payment method at checkout
2. On "Confirm Order", the extension creates an order via the NoPayn API
3. Customer is redirected to the NoPayn secure payment page
4. After payment, customer returns to your store with order status updated
5. A webhook ensures the order is updated even if the customer doesn't return

No card data touches your server — fully PCI DSS compliant.

## License

MIT
