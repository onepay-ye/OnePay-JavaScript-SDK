### 📦 OnePay JavaScript SDK
---

## **Simple & Fast Payment Gateway Loader**

The OnePay JavaScript SDK provides an easy and lightweight way to load and display available payment gateways in your application.

---

## 🔗 **JavaScript SDK – Required Script**

Include the SDK in your project:

```html
<script src="https://one-pay.info/api/sdk.js"></script>
```

---

## 🚀 **Usage Example**

### Load payment gateways using `getPaymentMethods()`

```javascript
document.getElementById('loadPaymentMethods').addEventListener('click', function() {

    if (window.OnePayLib) {

        // Initialize the SDK using your Merchant API key
        window.OnePayLib.initialize('65f3743a2f604');

        // Fetch available payment methods
        window.OnePayLib.getPaymentMethods()
            .then(methods => {
                console.log('Payment Methods:', methods);
            })
            .catch(error => {
                console.error('Error loading payment methods:', error);
            });

    } else {
        console.error('OnePay SDK is not loaded.');
    }

});
```

---

## 📥 **Sample JSON Response**

```json
{
    "status": 1,
    "message": [
        "jawali",
        "cashpay",
        "paypal"
    ]
}
```

---

## 📘 **Quick Explanation**

| Item                                 | Description                                             |
|--------------------------------------|---------------------------------------------------------|
| `OnePayLib.initialize(MERCHANT KEY)` | Activates the SDK using your MERCHANT API key.          |
| `OnePayLib.getPaymentMethods()`      | Returns the list of available payment gateways.         |
| `window.OnePayLib`                   | Ensures the SDK has been loaded before calling methods. |

---

## 🛠 **Requirements**

No additional libraries required — simply include the SDK script and start using it.

---

## 💡 **Notes**

- Make sure you have a valid **Merchant API Key** before calling the SDK.  
- A successful response includes `"status": 1`.  
- The `message` array contains the available payment gateways returned from the API.
