# Stock Portfolio Tracker

price = {"AAPL": 180, "TSLA": 250, "GOOG": 140, "AMZN": 130}
data = {}
n = int(input("Stocks count: "))

for i in range(n):
    s = input("Stock name: ").upper()
    q = int(input("Qty: "))
    if s in price:
        data[s] = q

total = 0
for s, q in data.items():
    total += price[s] * q
    print(f"{s}: {q} × ${price[s]} = ${price[s]*q}")

print("Total:", total)
