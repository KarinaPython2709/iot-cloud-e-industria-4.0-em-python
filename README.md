# iot-cloud-e-industria-4.0-em-python
projetos de extensão de IoT
Para a promoção de uma ferramenta portátil de segurança, foi desenvolvida uma solução 
com Arduino UNO R3, um sensor PIR (passive infrared sensor), três leds com o mesmo 
número de resistores, um Buzzer, uma protoboard, 13 jumpers e, diretamente no Arduino, 
uma bateria 9v conectada através de um adaptador.
A ideia era emitir dois sinais de alerta ao mesmo tempo quando fosse identificada qualquer 
movimentação dentro do range de ativação do sensor PIR, neste caso 7(sete) metros. Para 
isso, no firmware, ambos, leds e Buzzer, foram incluídos dentro do loop para sincronizar a 
ação destes com a ativação do sensor. 
Os leds foram montados em série e, dada a necessidade de aparecerem fora do recipiente 
que armazenava o Arduino e demais componentes, a conexão destes foi efetuada utilizando 
jumpers macho x fêmea, com as duas "pernas" do led sendo conectadas no lado fêmea do 
jumper.
O som do Buzzer foi configurado para se assemelhar ao som de um alarme convencional, 
sendo criado um laço de repetição que alterar entre as frequências de 1000hz e 500hz em 
um intervalo de 500ms.
Além disso, o delay do sensor de presença foi alterado para que mantivesse ativado ao 
menos 15 segundos após a última detecção de movimento, dessa forma estendendo os sinais 
de alerta.
