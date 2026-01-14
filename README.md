#include <stdio.h>

uint32_t temperature;
int main (void)
SPI_Init();
DelayInit();

while(i){
	
	DHT22_Init();
	
	response = Ethernet_GetReadings();
	
	if(response != Ethernet_RCV_OK)
		SPI_SendStr("Ethernet_GetReadings() error");
	SPI_SendInt(response);
} else
	response = Ethernet_DecodeReadings();
SPI_SendChar();

if((response & 0xff)!= (response >> 16))
	SPI_SendStr("Wrong data received.");
else {
	temperature = Ethernet_GetTemperature();
}
