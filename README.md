# Summary:
* This is a multi-purpose Python script to control an LED strip (WS2812B) ran off a Raspberry Pi via GPIO pins
  * If ran with a single argument of a color name, it changes the LED strip to that color
  * If ran with no arguments, it pings a host and changes to green or red to indicate uptime
  * The script can easily be called from a cron job that runs every minute to act as an interage outage detector. A cool use case is for LED strips in a server rack.
  * Example:
  *         sudo python GIOLED.py purple

* Feel free to repurpose as needed.

# Future plans:
* Maybe use curl or requests to get a color variable from my website, sanitize the input, then change to that color instead of just red/green if the variable was found
   * The website colors could also be controlled from a button on the page and/or discord API
   * Could also change state from pinging internal resources so that each server has a color and if that one has issues change to that color LED like color code errors for certain outages, DNS, high CPU, high fans, high power usage, etc.
