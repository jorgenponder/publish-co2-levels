# publish-co2-levels
A guide on to how to publish CO2 levels

Note! This is alpha code. And alpha instructions.

This is how you can publish the carbon dioxide levels of your premises in order to build some trust with the people who visit them. Five steps need to be done once, no running costs. The vision is to give out a USB or memory card and it just works, but right now you have to be comfortable installing python code on a computer.

This will be the result: https://mas.to/@koldio/109808222410697067

1. Get a TFA Dostmann CO2 meter, they cost around EUR 80 each. This meter is better than almost anything else in the price range, as it does not need to be adjusted (calibrated) once a day. Which means that it also works well in premises that are not fully ventilated every 24 hours. https://www.tfa-dostmann.de/en/product/co2-monitor-airco2ntrol-mini-31-5006/

2. Plug the meter into a computer with a USB cable. I have been using Linux.

3. Install the code from this repository: https://github.com/jorgenponder/tfa-airco2ntrol-mini It is a modified version of https://github.com/MathieuSchopfer/tfa-airco2ntrol-mini to provide 24 hour charts, as well save the diagram to disk instead of displaying it in a window

4. Get an account on a Mastodon server, and register an application there and save the keys for the application. Some Mastodon servers are supposed to be extra bot friendly, such as this one: https://botsin.space . But that server has a delay before getting approved. However you might still be waiting for a CO2 meter. Read the rules for the server you choose before opening an account there.

5. Install the code from this repository: https://github.com/jorgenponder/co2-data-publisher It uploads the image from the step 4 to your account on a Mastodon server every four hours. Or it does, if you put it in a cron job that runs it every four hours.

After this, your CO2 data should be published on a Mastodon account every four hours.
