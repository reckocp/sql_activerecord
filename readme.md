1.   51 users
``User.count``
2.   title: "Small Cotton Gloves",  title: "Small Wooden Computer",  title: "Awesome Granite Pants",  title: "Sleek Wooden Hat",  title: "Ergonomic Steel Car",
``Item.order('items.price DESC').limit(5)``
3.  title: "Ergonomic Granite Chair"
`Item.where(category: 'Books').order('items.price ASC').limit(1)``
4.  first_name: "Corrine", last_name: "Little"
``User.joins(:addresses).where(addresses: {street: '6439 Zetta Hills'}).take``
street: "54369 Wolff Forges", city: "Lake Bryon", state: "CA"
``Address.where(user_id: 40).limit(5)``
5. I changed it to Austin since we updated it to New York, NY yesterday.
``User.where(first_name: 'Virginie').take
Address.where(user_id: 39).take
Address.update(41, :city => "Austin", :state => "TX" )``
6. 7383
``tools = Item.where(category: "Tools")
tools.sum("price")``
7. 2129
``Order.sum("quantity")``
8. 420566
``Order.joins("JOIN items On orders.item_id = items.id").where("items.category = 'Books' ").sum("quantity*price")``
9.  id: 52, first_name: "Justin", last_name: "Herrick", email: "justin@theironyard.com">
``User.find_or_create_by(first_name: "Justin", last_name: "Herrick", email: "justin@theironyard.com")``
id: 379, user_id: 52, item_id: 25, quantity: 12, created_at: Tue, 29 Mar 2016 21:28:54 UTC +00:00>
``Order.find_or_create_by(user_id: 52, item_id: 25, quantity: 12, created_at: Time.now)``
