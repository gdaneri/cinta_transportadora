
conveyor belt arduino completed /*

Proyecto: Cinta transportadora con llenadora de líquidos

Componentes:

2 módulos L298N (motor DC y bomba de agua)no descartar uso de capacitores
2 sensores HW201 (infrarrojos)
LCD I2C 16x2: Conectar SDA a A4, SCL a A5 Alimentación 5V y GND
LEDs: LED Verde (D12) con resistencia 220Ω en serie LED Rojo (D11) con resistencia 220Ω en serie
Pulsador: Conectar un extremo a D7 y otro a GND
Resistencia pull-up interna activada en código
Funcionamiento:

Motor DC funciona hasta que Sensor1 detecta objeto
Se detiene motor DC, espera 3 segundos
Activa bomba de agua por 4 segundos
Se detiene bomba, espera 2 segundos
Reactiva motor DC hasta que Sensor2 detecta el objeto
Sensado de Nivel: Usa un sensor ultrasónico (HC-SR04) para medir la altura del líquido.
Comunicación Inalámbrica: Módulo Bluetooth (HC-05) para control remoto desde tu celular.
Registro de Datos: Guarda eventos en una tarjeta SD con fechas/horas.
Control por pulsador: - Pulsa el botón para pausar/reanudar todo el sistema - Los LEDs indican el estado actual *10. LCD muestra: - Línea 1: Estado de cinta y bomba - Línea 2: Contador de ciclos de llenado *11. Protecciones: - Debounce para el pulsador - Actualización eficiente del LCD
