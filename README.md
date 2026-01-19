# JavaScript-Day-5
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Tony's Café Bill</title>
    <style>
        body {
            background: #f4f1ec;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            padding-top: 50px;
        }

        .bill {
            background: #fff;
            width: 320px;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.2);
        }

        h2 {
            text-align: center;
            margin-bottom: 15px;
        }

        .line {
            display: flex;
            justify-content: space-between;
            margin: 6px 0;
        }

        .total {
            border-top: 2px dashed #000;
            margin-top: 10px;
            padding-top: 10px;
            font-weight: bold;
        }

        .note {
            margin-top: 10px;
            font-size: 13px;
            color: green;
            text-align: center;
        }
    </style>
</head>
<body>

<div class="bill">
    <h2> Tony’s Café Bill</h2>

    <div class="line">
        <span>Buggy Total ("200" + 50)</span>
        <span id="buggy"></span>
    </div>

    <div class="line">
        <span>Fixed Total (200 + 50)</span>
        <span id="fixed"></span>
    </div>

    <div class="line">
        <span>Extra Item (100.75)</span>
        <span id="extra"></span>
    </div>

    <div class="line total">
        <span>Final Total</span>
        <span id="final"></span>
    </div>

    <div class="note" id="stringTotal"></div>
</div>

<script>
    // Buggy values
    let item1 = "200";   // string
    let item2 = 50;      // number

    let buggyTotal = item1 + item2; // "20050"

    // Fix using Number()
    let fixedTotal = Number(item1) + item2; // 250

    // Extra item using parseFloat()
    let extraItem = parseFloat("100.75");

    let finalTotal = fixedTotal + extraItem; // 350.75

    // Convert final total to string
    let finalAsString = String(fixedTotal);

    // Display on UI
    document.getElementById("buggy").innerText = "₹ " + buggyTotal;
    document.getElementById("fixed").innerText = "₹ " + fixedTotal;
    document.getElementById("extra").innerText = "₹ " + extraItem;
    document.getElementById("final").innerText = "₹ " + finalTotal;

    document.getElementById("stringTotal").innerText =
        "Final total (as string): ₹" + finalAsString;
</script>

</body>
</html>


