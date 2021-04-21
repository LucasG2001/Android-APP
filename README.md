# Android-APP
Android Studio Projekt für meine BSC
Aufbau:
Im java/com.example.BLEAPP2 Ordner sind mehrere Klassen. Der code ist teilweise übernommen.

BatteryData: KLasse für Batterieinformationen (nicht relevant)

RecyclerBLEActivity: "This is a recycler activity that displays the list of the BLE devices available in the scan." Das funktioniert auch einwandfrei, könnte aber evtl mit andern BLE-Klassen interferieren.

BLERecyclerAdapter: This is an adapter that populates the list of BLE devices found in the sweep. This list is thenused to populate the UI the user sees so they can select the device they are working with. Funktioniert auch.

BluetoothLeService: Hier passieren die interessanten dinge. ServiceDiscovery, Charakteristiken lesen usw. Hier hängt sich das Programm beim lesen der Charakteristiken auf, bzw gatt.ReadCharacteristic() returned immer false, was nicht erfolgreich heisst.

GasData: Speichert Daten.

GattAttributes: Speichert die UUID's der gesuchten Charakteristiken und so weiter, was Android halt so an Hintergrundinfos braucht.

MaiunActivity: Standard MainActivity mit UI und so..

Funktionsweise: 

Mein Daten-sendendes Gerät liefert folgende charakteristiken: Einmal die X_acceleration, die sich kontinuierlich ändert und einmal die Y_acceleration, die konstant 2 ist. Dazu noch standerd Charakteristiken vom Bettery Service und Gerätinformationen. Die App sollte jetzt diese Daten kontinuierlich lesen (zumindest die x_acceleration) und anzeigen.

Danke dass du die das ansiehst :D
