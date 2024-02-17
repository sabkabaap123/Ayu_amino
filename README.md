from Vic_amino import Vic_Amino, Bot
import time
import vic_amino
community = "community URL"



client = BotAmino("email", "password", deviceId=aminofix.helpers.gen_deviceId())

user = client.get_from_code("user to pay coins to URL").objectId


bot = Bot(client,client.get_from_code(community).comId)

bot.add_influencer(user, 500)

amount_of_times_to_send_coins = 20 # calculated as: x * 500 : 100K = 200

print("Acc has " + str(client.get_wallet_info().totalCoins) + " coins")

print("logged in")
for i in range(0, amount_of_times_to_send_coins):
    bot.subscribe(user)
    print("Subscribed " + str(i) + " times")
    time.sleep(3)

bot.remove_influencer(user)
