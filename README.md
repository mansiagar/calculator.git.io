<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="calculator.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
    <!---header-->
    <style>
        main {
            width: 100%;
            height: 100vh;
            background-image: linear-gradient(#32dbdb, #17c8e3, #24b6f0, #218cde);
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }
        
        div {
            max-width: 500px;
            height: auto;
            background-color: #00cec9;
            padding: 30px;
            box-shadow: 1px 1px 15px 3px #2d3436;
        }
        
        h1 {
            margin-bottom: 10px;
            text-shadow: 1px 2px 1px white;
            text-transform: capitalize;
            text-align: center;
        }
        
        lable {
            display: block;
            text-transform: capitalize;
            margin-bottom: 10px;
        }
    </style>
</head>

<body>

    <main>
        <div>

            <h1>TIP Calculator</h1>
            <lable>BILL AMOUNT</lable>
            <input type="text" name="" id="bill_amount">
            <br>
            <lable> TIP PERCENTAGE</lable>
            <input type="text" name="" id="tip_perc">
            <br>
            <lable>TIP AMOUNT</lable>
            <input type="text" name="" id="tip_total" disabled>
            <br>
            <lable>TOTAL AMOUNT</lable>
            <input type="text" name="" id="total_billed" disabled>
            <br>

            <button onclick="tipcalcy()">TOTAL</button>


        </div>
    </main>
    <script>
        const tipcalcy = () => {
            let amount = document.getElementById('bill_amount').value;

            let PERCENTAGE = document.getElementById('tip_perc').value;

            const tip = PERCENTAGE * (amount / 100);

            let tipamount = document.getElementById('tip_total').value = tip;
            const totalAmount = tip + Number(amount);
            let totalbill = document.getElementById('total_billed').value = totalAmount;
        }
    </script>

</body>

</html>

</html>
