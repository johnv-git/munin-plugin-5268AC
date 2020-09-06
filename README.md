# munin-plugin-5268AC
Munin plugin for the (AT&T) Pace 5268AC ADSL Modem.

## Requirements
  * Munin
  * Perl
  * Bundle::LWP

## Usage
  * ln -s .../modem_stats_ /usr/local/etc/munin/plugins/modem_stats_(hostname)_(reporttype)

### Reports supported:
  * *uptime* - time since reboot in days
    * Uptime (days)
  * *version* - ATT config versions (silently updated)
    * Config
    * EAPOL_CERT
    * CMS_CERT
  * *speed* - DSL line rates
    * Line1 Speed Down
    * Line1 Speed Up
    * Line2 Speed Down
    * Line2 Speed Up
  * *snr* - DSL line metrics
    * Line1 SNR Down
    * Line1 SNR Up
    * Line1 Attenuation Down
    * Line1 Attenuation Up
    * Line1 Power Down
    * Line1 Power Up
    * Line2 SNR Down
    * Line2 SNR Up
    * Line2 Attenuation Down
    * Line2 Attenuation Up
    * Line2 Power Down
    * Line2 Power Up
  * *wanbytes* - WAN traffic in bytes
    * WAN bps Up/Down
  * *wanpackets* - WAN traffic in packets
    * WAN pps Up/Down
  * *wanerrors* - WAN packet errors
    * WAN errors Up/Down
  * *lanbytes* - LAN traffic in bytes
    * Port1 bps Up/Down
    * Port2 bps Up/Down
    * Port3 bps Up/Down
    * Port4 bps Up/Down
  * *lanpackets* - LAN traffic in packets
    * Port1 pps Up/Down
    * Port2 pps Up/Down
    * Port3 pps Up/Down
    * Port4 pps Up/Down
  * *lanerrors* - LAN packet errors
    * Port1 errors Up/Down
    * Port2 errors Up/Down
    * Port3 errors Up/Down
    * Port4 errors Up/Down
  * *wifibytes* - WIFI traffic in bytes
    * 2.4Ghz bps Up/Down
    * 5.0Ghz bps Up/Down
  * *wifipackets* - WIFI traffic in packets
    * 2.4Ghz pps Up/Down
    * 5.0Ghz pps Up/Down
  * *wifierrors* - WIFI packet errors
    * 2.4Ghz errors Up/Down
    * 5.0Ghz errors Up/Down

### Interpreting Charts:
In general, this is useful to detect line degradation over time.  Perhaps the copper to your house does poorly in the
rain.  Perhaps your dsl is unstable after the neighbor had their phone installed.  Perhaps you lose sync every night
because someone turns on a massive RF-generating dimmer switch.

### Notes:
This hasn't been tested on a single line service.

### TODO:
* parse/report landiscards
* parse/report wifidiscards
