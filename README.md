rint('-' * 46)
print("*** Welcome to Beverage Wholesale Program! ***")
print('-' * 46)

#Display menu
print("Please select the type of purchase: ")
print("C: Coffee Beans")
print("T: Tea Boxes")

#Invalid input for tea and coffee
customer_order = input(">>> ")
if customer_order.lower() !="c" and customer_order.lower() !="t":
   print ("Invalid input, you should enter c/C or t/T")
   exit ()

#Coffee and tea process
if customer_order.lower() == "c":
   coffee_kg = float(input('Enter the number of kilograms (kg) of coffee: '))
   if coffee_kg <=0:
      print('Quantity of coffee should be>0')
elif customer_order.lower() == "t":
   tea_box = float(input('Enter the number of boxes of tea: '))
else:
   print('Invalid input') and exit

#Calculate coffee price before and after discounted
coffee_price_before_discounted = coffee_kg * 18.50
coffee_price_after_discounted = coffee_price_before_discounted * 0.9

#Calculate tea price before and after discounted
tea_price_before_discounted = tea_box * 0.45 * 20
tea_price_after_discounted = tea_box * 0.85

#Get province
province = input("Please enter the 2-letter province abbrevation: ")

if province.lower() == "AB" or province.lower() == "BC":
   coffee_price_gst = coffee_price_after_discounted * 0.05
   tea_price_gst = tea_price_after_discounted * 0.05
elif province.lower() =="ON":
   coffee_price_gst = coffee_price_after_discounted * 0.13
   tea_price_gst = tea_price_after_discounted * 0.13
else:
   coffee_price_gst = coffee_price_after_discounted * 0.15
   tea_price_gst = tea_price_after_discounted * 0.15
