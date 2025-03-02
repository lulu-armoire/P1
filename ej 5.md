# 📌 Informe de Funcionamiento del Código de Interrupción con Botón en ESP32-S3  

## 📖 Descripción del Código  
Este programa usa una **interrupción externa** en el **pin 18** para detectar pulsaciones de un botón. Cada vez que el botón es presionado, el código:  
1. **Incrementa un contador** de pulsaciones.  
2. **Muestra el número de presiones** en el monitor serie.  
3. **Desactiva la interrupción después de 1 minuto**.  

---

## ⚙️ Configuración  
- **Placa:** ESP32-S3  
- **Botón:** Conectado al **pin 18**  
- **Modo del pin:** `INPUT_PULLUP` (usa la resistencia interna pull-up del ESP32)  
- **Interrupción:** Activada en **FALLING**, es decir, cuando el botón pasa de **HIGH a LOW**.  

---

## 🔄 Flujo de Ejecución  
1. Se inicia la comunicación serie a **115200 baudios**.  
2. Se configura el **pin 18 como entrada con pull-up**.  
3. Se asigna una **interrupción** que detecta cuando el botón es presionado.  
4. Cada vez que se presiona el botón:  
   - Se incrementa el contador.  
   - Se imprime en el **monitor serie** cuántas veces se ha presionado.  
5. **Después de 1 minuto**, la interrupción se desactiva y ya no se detectan más pulsaciones.  

---

## 🖥️ Salidas en el Monitor Serie  
Si el usuario presiona el botón varias veces, el monitor serie mostrará algo como:  



> Written with [StackEdit](https://staenter code hereckedit.io/).`enter code here`
