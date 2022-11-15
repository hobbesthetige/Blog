### Backstory ###

When the Avenue app first launched in 2019, its primary purpose was to be a route optimization tool for small business owners who made a lot of stops throughout their day. For instance, a good friend of mine with a lawn care business could input all of the customers he needed to mow at throughout his day, and the app would package this data up to a traveling salesman algorithm API that analyized traffic patterns and other factors to determine the best order for each stop. After a year of COVID almost killing our service, what we learned is that there are more people who already know the general *order* they need to travel, but it would be more helpful to connect to their scheduling service to provide that information to them on their mobile device. So we scratched the traveling salesman API, rewrote the app in updated SwiftUI, and set out to connect with 3rd party scheduling services like HouseCallPro. We still have a way to lookup customers from your contacts/address book or Google maps within the app, but our real value-add now was getting a list of your scheduled stops and presenting them in a meaningful way to customers. The timing couldn't have been better for Apple to open up Carplay to developers.


By connecting our app to Carplay, we have the advantage of showing all of your stops in a list overlayed on a map. Tapping on each stop provides the stop details pulled from your CRM/ERM, and we have two easy "Navigate" and "Complete Stop" buttons that make it super easy to kick off driving directions and mark a stop as complete.

### Getting Started ###

We didn't expect to have to *apply* to Apple for a Carplay entitlement, but they responded within two business days and approved our request to add Carplay capabilities to the Avenue App. Getting the entitlement added was easy, but making the adjustments to the XCode project felt a little rough around the edges from Apple's documentation. Suffice it to say that documentation and user guides are in the infant stages for Apple as well. 


Our first challenge was getting the Carplay Simulator to work. There are two ways that Apple gives you to start off: adding a Carplay screen to your simulator, and a standalone radio head unit simulator app that runs on your Mac and requires connecting a USB cable. It would have been great if either of those options worked right out of the box, but we had difficulty getting either to work consistently and reliably. The iPhone simulator Carplay screen simply refused to work at all, and we spent way too long troubleshooting only to realize it was very buggy. The head unit simulator app was buggy as well, and never consistently recognized the iPhone when it was connected to USB. 
    
### Carplay Head Unit

After much frustration with simulators, we decided to purchase a portable Carplay head unit that could sit on our desk. This was a great choice, as it played into our business model of providing external units for customers who did not have Carplay already installed in their service vehicles. 

The unit we selected as our demo was the Road Top Wireless Carplay & Android Auto Portable Receiver [Amazon](https://www.amazon.com/dp/B09P8C5V26?psc=1&ref=ppx_yo2ov_dt_b_product_details):

    Road Top Wireless Carplay & Android Auto, Wireless Mirroring Portable 8.8" Touchscreen Car Radio Receiver with Siri, Mic, Bluetooth 5.0, WiFi, FM, GPS Navigation Dash Windshield Mounted
 
What we liked is that the screen was very high quality, we liked the width-to-height ratio, and it supported wireless Carplay. RoadTop also had a number of solid reviews that made us more confident that it was a good decision.
 
We quickly ran into our second setback when we realized that our newly purchased unit was meant for a *vehicle*, and it didn't have an A/C adaptor, only a cigarette charger. We bought a universal A/C adaptor that flexes on voltage and tip sizes [Amazon](https://www.amazon.com/dp/B09WMS6K9C?psc=1&ref=ppx_yo2ov_dt_b_product_details).
    
    Arkare 30W Universal AC to DC Power Adapter Adjustable Power Supply 3V 4.5V 6V 9V 12V 2A 1A DC Adapter AC 100-240V to DC 3-12V Multi Voltage Switching Power Adapter with 15 Tips + Polarity Converter
    
