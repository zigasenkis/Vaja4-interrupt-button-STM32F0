# Vaja4-interrupt-button-STM32F0

Q/ 2b) Glede na vašo razvojno ploščico in razširitveno vezje s tipkami, izberite ustrezen digitalni vhod kot
   interrupt (GPIO_EXT…) in izhod za zeleno LED. Zapišite izbrana pina:

A/ Za interupt pin sva izbrala pin PA0 in za izhod za zeleno LED PC9.

Q/ 3d) Znotraj te funkcije zapišite ukaz za vklop/izklop zelene LED (pomagajte si z metodo toggle, glej vaja0a).

A/ HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_9)
   for(uint32_t i=0; i<10000; i++);

Q/ 3e) Znotraj iste funkcije dodajte še zakasnitev, ki je potrebna, ko uporabimo mehanska tipkala/stikala:
   for(uint32_t i=0; i<10000; i++);
   Koliko znaša (v mili sekundah) zapisana zakasnitev?

A/ 10 mikrosekund.

Q/ 3f) V user code begin 3 - zanka while(1) - zapišite ukaz za utripanje modre LED (metoda toggle, glej vaja0a):

A/ HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_8);

Q/ 3g) V to zanko dodajte ukaz za zakasnitev z funkcijo Delay iz knjižnice HAL, in sicer pol sekunde (glej vaja0a):

A/ HAL_Delay(500);

Q/ 4b) Opazujte delovanje (utripanje modre LED). Kaj se zgodi, ko pritisnemo na modro tipko na STM32F0?

A/ Ko pritisneš modro tipko na STM32F0 se takoj prižge zelena LED luč a modra vedno utripa enako.

Q/ 4c) Ali pritisk na modro tipko vpliva na utripanje modre LED in zakaj?

A/ Ne, pritisk na modro tipko ne vpliva na utripanje modre LED, ker smo v programu naredili tako, da modra tipka prižge samo zeleno LED.
