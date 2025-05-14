WiFi
aircrack-ng wifi.cap 
sudo gunzip /usr/share/wordlists/rockyou.txt.gz
aircrack-ng -w /usr/share/wordlists/rockyou.txt -b 02:1A:11:FF:D9:BD wifi.cap

Bluetooth
crackle -i bt.pcap -o dbt.pcap

MQTT-IoT
tshark -r mqtt.cap -Y "mqtt" -T fields -e mqtt.topic
tshark -r mqtt.cap -Y "mqtt" -T fields -e mqtt.msg
echo "48656c6c6f2066726f6d20746865205061686f20626c6f636b696e6720636c69656e74" | xxd -r -p
