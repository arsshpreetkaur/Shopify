# Shopify Coding!

HTML CODE⭐

<!DOCTYPE html>
<html>
  <head>
    <title>Vintage Key Store</title>
  </head>
  <body>
    <h1>Welcome to our key's Store</h1>
    </body
</html>


INTRODUCTION CODE⭐

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vinny's Vintage Keys</title>
    <style>
        /* Add some basic styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px;
        }
        .header, .footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 10px 0;
        }
        .products {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
        }
        .product {
            width: 30%;
            margin: 10px;
            padding: 10px;
            border: 1px solid #ccc;
            text-align: center;
        }
        .product img {
            width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Vinny's Vintage Keys</h1>
    </div>
    <div class="container">
        <section id="about">
            <h2>About Us</h2>
            <p id="description"></p>
        </section>
        <section id="products">
            <h2>Featured Products</h2>
            <div class="products" id="featured-products"></div>
        </section>
    </div>
    <div class="footer">
        <p>Contact us: <span id="contact-email"></span> | Phone: <span id="contact-phone"></span></p>
        <p>Address: <span id="contact-address"></span></p>
    </div>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            // Your JSON data as a string
            const jsonData = `{
                "store": {
                    "name": "Vinny's Vintage Keys",
                    "description": "Discover the finest collection of vintage keys and key-related memorabilia. Our store offers a curated selection of unique and rare keys from different eras, perfect for collectors and enthusiasts.",
                    "contact": {
                        "email": "info@vintagekeys.com",
                        "phone": "(123) 456-7890",
                        "address": "123 Vintage Lane, History Town, USA",
                        "social": {
"twitter": "https://twitter.com/vintagekeys",
"facebook": "https://facebook.com/vintagekeys",
"pinterest": "https://pinterest.com/vintagekeys",
"instagram": "https://instagram.com/vintagekeys"
                        }
                    }
                },
                "featuredProducts": [
                    {
                        "id": 1,
                        "name": "Vintage Key 1",
                        "description": "A unique vintage key from the 19th century, perfect for collectors.",
"image": "https://i.ebayimg.com/images/g/xSUAAOSw3u9fAVy4/s-l400.jpg"
                    },
                    {
                        "id": 2,
                        "name": "Vintage Key 2",
                        "description": "An exquisite vintage key with intricate designs.",
"image": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcStQP7MsaN6KS8em7LSpcttKW6jp_Ho8GJ-Eel84RRDOoxdC7kCPNd4GqBgM0CMH0fYRFU&usqp=CAU"
                    },
                    {
                        "id": 3,
                        "name": "Vintage Key 3",
                        "description": "A rare vintage key with a fascinating history.",
"image": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT06NE7MkAfcVju_885WymfTTrjEuIQKAo6NEO0Bzmos52qLLS6K39iYMMWlnlZxBqML6Y&usqp=CAU"
                    }
                ]
            }`;
 
            // Parse the JSON string into a JavaScript object
            const data = JSON.parse(jsonData);
 
            // Populate the description
            document.getElementById('description').innerText = data.store.description;
 
            // Populate the contact information
document.getElementById('contact-email').innerText = data.store.contact.email;
            document.getElementById('contact-phone').innerText = data.store.contact.phone;
            document.getElementById('contact-address').innerText = data.store.contact.address;
 
            // Populate the featured products
            const productsContainer = document.getElementById('featured-products');
            data.featuredProducts.forEach(product => {
                const productElement = document.createElement('div');
                productElement.className = 'product';
                productElement.innerHTML = `
<img src="${product.image}" alt="${product.name}">
${product.name}</h3>
                    <p>${product.description}</p>
                `;
                productsContainer.appendChild(productElement);
            });
        });
    </script>
</body>
</html>
