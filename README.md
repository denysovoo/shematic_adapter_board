FTDI’s Synchronous FIFO interface is used to perform data transfer between FPGA and host PC. As the operation is Synchronous, the data transfers occur in synchronisation with clock. The speed is much higher than that of asynchronous FIFO. To use the synchronous FIFO transfer mode available on FT2232H, its hardware and driver must be configured as 245 FIFO and D2XX respectively. In this article, Channel A of FT2232H is configured as FIFO, which provides the following signals: 

data: It is bi-directional bus carrying the 8-bit FIFO data. 

rxf_n: It is an active low signal. When de-asserted, does not read data from FIFO. When it is enabled, it indicates that there is some data available in FIFO, the data is read after asserting rd_n. 

txe_n: It is an active low signal. When de-asserted, does not write data to FIFO. When it is asserted, data can be written to FIFO if wr_n is asserted. 

rd_n: It is an active low signal. When asserted, data is driven onto data bus from FIFO. 

wr_n: It is an active low signal. When asserted, data written on data bus is driven into FIFO. 

oe_n: it is an active ow output enable input signal. When asserted, data is driven ondata bus, then rd_n is enable after 1 clock period.



Connect the CON4 connector to the GPIO1 connector of the DE0-Nano-SoC board.

Connector CON1 with arduino connector card DE0-Nano-SoC.

Connector CON2 with connector CN2 FT2232H.

Connector CON3 with connector CN3 FT2232H.


This description of the debugging boards for which the adapter was made
https://www.terasic.com.tw/attachment/archive/941/DE0-Nano-SoC_User_manual.pdf
http://www.ftdichip.com/Support/Documents/DataSheets/Modules/DS_FT2232H_Mini_Module.pdf
