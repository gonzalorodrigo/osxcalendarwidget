# osxcalendarwidget

The osX weather widget (old fashion dashboard) fails loading depending on the network connection and other conditions.
It appears to freeze and not load any data. The reality is that the data connection gets broken due to incompatibility modes
between the server and the client. In order to avoid this, it is required to modify the parser file used by this widget.

In summary, if your weather widget does not work just add the modifictions of weatherParser.js (added in commit e44cd39dd782105e01f312b704ab87da8c782dfe)
to the file /System/Library/WidgetResources/.parsers/weatherParser.js

To modify this file you may need to disable the integrity control (or install the widget and parser in user space) with:
- Reboot and press "command+r" when the apple chime sounds.
- Open terminal.
- csrutil disable; reboot

Good Luck!
