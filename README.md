# homebridge-pet-feeder

Homebridge plugin to feed the kitties.  In my case, this is using the new Wio Link, which just has a REST endpoint to change device state.  The device itself has an attached grove relay that runs a DC motor to actuate the feeder. 

## Installation

Naturally...
```
npm install -g homebridge-pet-feeder
```

## Configuration

Add this to your `~/.homebridge/config.json` as an accessory:
```
{
  "accessory": "PetFeeder",
  "name": "Kitty Feeder",
  "onCommand": "https://iot.seeed.cc/v1/node/GroveRelayD0/onoff/1?access_token=YOUR_GROVE_ACCESS_TOKEN",
  "offCommand": "https://iot.seeed.cc/v1/node/GroveRelayD0/onoff/0?access_token=YOUR_GROVE_ACCESS_TOKEN"
  "duration": 3000
}
```

# DISCLAIMER

Don't be a derp derp and rely on this to feed your kitties for you.  This is just an experiment, and a means to get the little shits to stop yelling at me two hours before mealtime.  If you are trusting this plugin with Jinxy or Fido's life, a super secret embedded module will call PETA and tell them you're a horrible person.  

![Please don't use node to feed me...](https://raw.githubusercontent.com/arcreative/homebridge-pet-feeder/master/sadcat.jpg)

Now... Enjoy!
