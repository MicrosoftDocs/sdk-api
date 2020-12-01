---
UID: NS:winbase._COMMPROP
title: COMMPROP (winbase.h)
description: Contains information about a communications driver.
helpviewer_keywords: ["*LPCOMMPROP","BAUD_075","BAUD_110","BAUD_115200","BAUD_1200","BAUD_128K","BAUD_134_5","BAUD_14400","BAUD_150","BAUD_1800","BAUD_19200","BAUD_2400","BAUD_300","BAUD_38400","BAUD_4800","BAUD_56K","BAUD_57600","BAUD_600","BAUD_7200","BAUD_9600","BAUD_USER","COMMPROP","COMMPROP structure","DATABITS_16","DATABITS_16X","DATABITS_5","DATABITS_6","DATABITS_7","DATABITS_8","LPCOMMPROP","LPCOMMPROP structure pointer","PARITY_EVEN","PARITY_MARK","PARITY_NONE","PARITY_ODD","PARITY_SPACE","PCF_16BITMODE","PCF_DTRDSR","PCF_INTTIMEOUTS","PCF_PARITY_CHECK","PCF_RLSD","PCF_RTSCTS","PCF_SETXCHAR","PCF_SPECIALCHARS","PCF_TOTALTIMEOUTS","PCF_XONXOFF","PST_FAX","PST_LAT","PST_MODEM","PST_NETWORK_BRIDGE","PST_PARALLELPORT","PST_RS232","PST_RS422","PST_RS423","PST_RS449","PST_SCANNER","PST_TCPIP_TELNET","PST_UNSPECIFIED","PST_X25","SP_BAUD","SP_DATABITS","SP_HANDSHAKING","SP_PARITY","SP_PARITY_CHECK","SP_RLSD","SP_STOPBITS","STOPBITS_10","STOPBITS_15","STOPBITS_20","_COMMPROP","_win32_commprop_str","base.commprop_str","winbase/COMMPROP","winbase/LPCOMMPROP"]
old-location: base\commprop_str.htm
tech.root: base
ms.assetid: d50ff606-1939-4e36-ba83-da8f269a3cc8
ms.date: 12/05/2018
ms.keywords: '*LPCOMMPROP, BAUD_075, BAUD_110, BAUD_115200, BAUD_1200, BAUD_128K, BAUD_134_5, BAUD_14400, BAUD_150, BAUD_1800, BAUD_19200, BAUD_2400, BAUD_300, BAUD_38400, BAUD_4800, BAUD_56K, BAUD_57600, BAUD_600, BAUD_7200, BAUD_9600, BAUD_USER, COMMPROP, COMMPROP structure, DATABITS_16, DATABITS_16X, DATABITS_5, DATABITS_6, DATABITS_7, DATABITS_8, LPCOMMPROP, LPCOMMPROP structure pointer, PARITY_EVEN, PARITY_MARK, PARITY_NONE, PARITY_ODD, PARITY_SPACE, PCF_16BITMODE, PCF_DTRDSR, PCF_INTTIMEOUTS, PCF_PARITY_CHECK, PCF_RLSD, PCF_RTSCTS, PCF_SETXCHAR, PCF_SPECIALCHARS, PCF_TOTALTIMEOUTS, PCF_XONXOFF, PST_FAX, PST_LAT, PST_MODEM, PST_NETWORK_BRIDGE, PST_PARALLELPORT, PST_RS232, PST_RS422, PST_RS423, PST_RS449, PST_SCANNER, PST_TCPIP_TELNET, PST_UNSPECIFIED, PST_X25, SP_BAUD, SP_DATABITS, SP_HANDSHAKING, SP_PARITY, SP_PARITY_CHECK, SP_RLSD, SP_STOPBITS, STOPBITS_10, STOPBITS_15, STOPBITS_20, _COMMPROP, _win32_commprop_str, base.commprop_str, winbase/COMMPROP, winbase/LPCOMMPROP'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: COMMPROP, *LPCOMMPROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COMMPROP
 - winbase/_COMMPROP
 - LPCOMMPROP
 - winbase/LPCOMMPROP
 - COMMPROP
 - winbase/COMMPROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - COMMPROP
---

# COMMPROP structure


## -description

Contains information about a communications driver.

## -struct-fields

### -field wPacketLength

The size of the entire data packet, regardless of the amount of data requested, in bytes.

### -field wPacketVersion

The version of the structure.

### -field dwServiceMask

A bitmask indicating which services are implemented by this provider. The 
      <b>SP_SERIALCOMM</b> value is always specified for communications providers, including modem 
      providers.

### -field dwReserved1

Reserved; do not use.

### -field dwMaxTxQueue

The maximum size of the driver's internal output buffer, in bytes. A value of zero indicates that no 
      maximum value is imposed by the serial provider.

### -field dwMaxRxQueue

The maximum size of the driver's internal input buffer, in bytes. A value of zero indicates that no maximum 
      value is imposed by the serial provider.

### -field dwMaxBaud

The maximum allowable baud rate, in bits per second (bps). This member can be one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BAUD_075"></a><a id="baud_075"></a><dl>
<dt><b>BAUD_075</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
75 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_110"></a><a id="baud_110"></a><dl>
<dt><b>BAUD_110</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
110 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_134_5"></a><a id="baud_134_5"></a><dl>
<dt><b>BAUD_134_5</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
134.5 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_150"></a><a id="baud_150"></a><dl>
<dt><b>BAUD_150</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
150 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_300"></a><a id="baud_300"></a><dl>
<dt><b>BAUD_300</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
300 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_600"></a><a id="baud_600"></a><dl>
<dt><b>BAUD_600</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
600 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_1200"></a><a id="baud_1200"></a><dl>
<dt><b>BAUD_1200</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
1200 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_1800"></a><a id="baud_1800"></a><dl>
<dt><b>BAUD_1800</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
1800 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_2400"></a><a id="baud_2400"></a><dl>
<dt><b>BAUD_2400</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
2400 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_4800"></a><a id="baud_4800"></a><dl>
<dt><b>BAUD_4800</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
4800 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_7200"></a><a id="baud_7200"></a><dl>
<dt><b>BAUD_7200</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
7200 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_9600"></a><a id="baud_9600"></a><dl>
<dt><b>BAUD_9600</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
9600 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_14400"></a><a id="baud_14400"></a><dl>
<dt><b>BAUD_14400</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
14400 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_19200"></a><a id="baud_19200"></a><dl>
<dt><b>BAUD_19200</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
19200 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_38400"></a><a id="baud_38400"></a><dl>
<dt><b>BAUD_38400</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
38400 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_56K"></a><a id="baud_56k"></a><dl>
<dt><b>BAUD_56K</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
56K bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_57600"></a><a id="baud_57600"></a><dl>
<dt><b>BAUD_57600</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
57600 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_115200"></a><a id="baud_115200"></a><dl>
<dt><b>BAUD_115200</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
115200 bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_128K"></a><a id="baud_128k"></a><dl>
<dt><b>BAUD_128K</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
128K bps

</td>
</tr>
<tr>
<td width="40%"><a id="BAUD_USER"></a><a id="baud_user"></a><dl>
<dt><b>BAUD_USER</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Programmable baud rate.

</td>
</tr>
</table>

### -field dwProvSubType

The communications-provider type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PST_FAX"></a><a id="pst_fax"></a><dl>
<dt><b>PST_FAX</b></dt>
<dt>0x00000021</dt>
</dl>
</td>
<td width="60%">
FAX device

</td>
</tr>
<tr>
<td width="40%"><a id="PST_LAT"></a><a id="pst_lat"></a><dl>
<dt><b>PST_LAT</b></dt>
<dt>0x00000101</dt>
</dl>
</td>
<td width="60%">
LAT protocol

</td>
</tr>
<tr>
<td width="40%"><a id="PST_MODEM"></a><a id="pst_modem"></a><dl>
<dt><b>PST_MODEM</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
Modem device

</td>
</tr>
<tr>
<td width="40%"><a id="PST_NETWORK_BRIDGE"></a><a id="pst_network_bridge"></a><dl>
<dt><b>PST_NETWORK_BRIDGE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Unspecified network bridge

</td>
</tr>
<tr>
<td width="40%"><a id="PST_PARALLELPORT"></a><a id="pst_parallelport"></a><dl>
<dt><b>PST_PARALLELPORT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Parallel port

</td>
</tr>
<tr>
<td width="40%"><a id="PST_RS232"></a><a id="pst_rs232"></a><dl>
<dt><b>PST_RS232</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
RS-232 serial port

</td>
</tr>
<tr>
<td width="40%"><a id="PST_RS422"></a><a id="pst_rs422"></a><dl>
<dt><b>PST_RS422</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
RS-422 port

</td>
</tr>
<tr>
<td width="40%"><a id="PST_RS423"></a><a id="pst_rs423"></a><dl>
<dt><b>PST_RS423</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
RS-423 port

</td>
</tr>
<tr>
<td width="40%"><a id="PST_RS449"></a><a id="pst_rs449"></a><dl>
<dt><b>PST_RS449</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
RS-449 port

</td>
</tr>
<tr>
<td width="40%"><a id="PST_SCANNER"></a><a id="pst_scanner"></a><dl>
<dt><b>PST_SCANNER</b></dt>
<dt>0x00000022</dt>
</dl>
</td>
<td width="60%">
Scanner device

</td>
</tr>
<tr>
<td width="40%"><a id="PST_TCPIP_TELNET"></a><a id="pst_tcpip_telnet"></a><dl>
<dt><b>PST_TCPIP_TELNET</b></dt>
<dt>0x00000102</dt>
</dl>
</td>
<td width="60%">
TCP/IP Telnet protocol

</td>
</tr>
<tr>
<td width="40%"><a id="PST_UNSPECIFIED"></a><a id="pst_unspecified"></a><dl>
<dt><b>PST_UNSPECIFIED</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Unspecified

</td>
</tr>
<tr>
<td width="40%"><a id="PST_X25"></a><a id="pst_x25"></a><dl>
<dt><b>PST_X25</b></dt>
<dt>0x00000103</dt>
</dl>
</td>
<td width="60%">
X.25 standards

</td>
</tr>
</table>

### -field dwProvCapabilities

A bitmask indicating the capabilities offered by the provider. This member can be a combination of the 
      following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PCF_16BITMODE"></a><a id="pcf_16bitmode"></a><dl>
<dt><b>PCF_16BITMODE</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Special 16-bit mode supported

</td>
</tr>
<tr>
<td width="40%"><a id="PCF_DTRDSR"></a><a id="pcf_dtrdsr"></a><dl>
<dt><b>PCF_DTRDSR</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
DTR (data-terminal-ready)/DSR (data-set-ready) supported

</td>
</tr>
<tr>
<td width="40%"><a id="PCF_INTTIMEOUTS"></a><a id="pcf_inttimeouts"></a><dl>
<dt><b>PCF_INTTIMEOUTS</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Interval time-outs supported

</td>
</tr>
<tr>
<td width="40%"><a id="PCF_PARITY_CHECK"></a><a id="pcf_parity_check"></a><dl>
<dt><b>PCF_PARITY_CHECK</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Parity checking supported

</td>
</tr>
<tr>
<td width="40%"><a id="PCF_RLSD"></a><a id="pcf_rlsd"></a><dl>
<dt><b>PCF_RLSD</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
RLSD (receive-line-signal-detect) supported

</td>
</tr>
<tr>
<td width="40%"><a id="PCF_RTSCTS"></a><a id="pcf_rtscts"></a><dl>
<dt><b>PCF_RTSCTS</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
RTS (request-to-send)/CTS (clear-to-send) supported

</td>
</tr>
<tr>
<td width="40%"><a id="PCF_SETXCHAR"></a><a id="pcf_setxchar"></a><dl>
<dt><b>PCF_SETXCHAR</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Settable XON/XOFF supported

</td>
</tr>
<tr>
<td width="40%"><a id="PCF_SPECIALCHARS"></a><a id="pcf_specialchars"></a><dl>
<dt><b>PCF_SPECIALCHARS</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Special character support provided

</td>
</tr>
<tr>
<td width="40%"><a id="PCF_TOTALTIMEOUTS"></a><a id="pcf_totaltimeouts"></a><dl>
<dt><b>PCF_TOTALTIMEOUTS</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
The total (elapsed) time-outs supported

</td>
</tr>
<tr>
<td width="40%"><a id="PCF_XONXOFF"></a><a id="pcf_xonxoff"></a><dl>
<dt><b>PCF_XONXOFF</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
XON/XOFF flow control supported

</td>
</tr>
</table>

### -field dwSettableParams

A bitmask indicating the communications parameters that can be changed. This member can be a combination of 
      the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SP_BAUD"></a><a id="sp_baud"></a><dl>
<dt><b>SP_BAUD</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Baud rate

</td>
</tr>
<tr>
<td width="40%"><a id="SP_DATABITS"></a><a id="sp_databits"></a><dl>
<dt><b>SP_DATABITS</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Data bits

</td>
</tr>
<tr>
<td width="40%"><a id="SP_HANDSHAKING"></a><a id="sp_handshaking"></a><dl>
<dt><b>SP_HANDSHAKING</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Handshaking (flow control)

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PARITY"></a><a id="sp_parity"></a><dl>
<dt><b>SP_PARITY</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Parity

</td>
</tr>
<tr>
<td width="40%"><a id="SP_PARITY_CHECK"></a><a id="sp_parity_check"></a><dl>
<dt><b>SP_PARITY_CHECK</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Parity checking

</td>
</tr>
<tr>
<td width="40%"><a id="SP_RLSD"></a><a id="sp_rlsd"></a><dl>
<dt><b>SP_RLSD</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
RLSD (receive-line-signal-detect)

</td>
</tr>
<tr>
<td width="40%"><a id="SP_STOPBITS"></a><a id="sp_stopbits"></a><dl>
<dt><b>SP_STOPBITS</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Stop bits

</td>
</tr>
</table>

### -field dwSettableBaud

The baud rates that can be used. For values, see the <b>dwMaxBaud</b> member.

### -field wSettableData

A bitmask indicating the number of data bits that can be set. This member can be a combination of the 
      following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DATABITS_5"></a><a id="databits_5"></a><dl>
<dt><b>DATABITS_5</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
5 data bits

</td>
</tr>
<tr>
<td width="40%"><a id="DATABITS_6"></a><a id="databits_6"></a><dl>
<dt><b>DATABITS_6</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
6 data bits

</td>
</tr>
<tr>
<td width="40%"><a id="DATABITS_7"></a><a id="databits_7"></a><dl>
<dt><b>DATABITS_7</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
7 data bits

</td>
</tr>
<tr>
<td width="40%"><a id="DATABITS_8"></a><a id="databits_8"></a><dl>
<dt><b>DATABITS_8</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
8 data bits

</td>
</tr>
<tr>
<td width="40%"><a id="DATABITS_16"></a><a id="databits_16"></a><dl>
<dt><b>DATABITS_16</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
16 data bits

</td>
</tr>
<tr>
<td width="40%"><a id="DATABITS_16X"></a><a id="databits_16x"></a><dl>
<dt><b>DATABITS_16X</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Special wide path through serial hardware lines

</td>
</tr>
</table>

### -field wSettableStopParity

A bitmask indicating the stop bit and parity settings that can be selected. This member can be a 
      combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STOPBITS_10"></a><a id="stopbits_10"></a><dl>
<dt><b>STOPBITS_10</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
1 stop bit

</td>
</tr>
<tr>
<td width="40%"><a id="STOPBITS_15"></a><a id="stopbits_15"></a><dl>
<dt><b>STOPBITS_15</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
1.5 stop bits

</td>
</tr>
<tr>
<td width="40%"><a id="STOPBITS_20"></a><a id="stopbits_20"></a><dl>
<dt><b>STOPBITS_20</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
2 stop bits

</td>
</tr>
<tr>
<td width="40%"><a id="PARITY_NONE"></a><a id="parity_none"></a><dl>
<dt><b>PARITY_NONE</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
No parity

</td>
</tr>
<tr>
<td width="40%"><a id="PARITY_ODD"></a><a id="parity_odd"></a><dl>
<dt><b>PARITY_ODD</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Odd parity

</td>
</tr>
<tr>
<td width="40%"><a id="PARITY_EVEN"></a><a id="parity_even"></a><dl>
<dt><b>PARITY_EVEN</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
Even parity

</td>
</tr>
<tr>
<td width="40%"><a id="PARITY_MARK"></a><a id="parity_mark"></a><dl>
<dt><b>PARITY_MARK</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
Mark parity

</td>
</tr>
<tr>
<td width="40%"><a id="PARITY_SPACE"></a><a id="parity_space"></a><dl>
<dt><b>PARITY_SPACE</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Space parity

</td>
</tr>
</table>

### -field dwCurrentTxQueue

The size of the driver's internal output buffer, in bytes. A value of zero indicates that the value is 
      unavailable.

### -field dwCurrentRxQueue

The size of the driver's internal input buffer, in bytes. A value of zero indicates that the value is 
      unavailable.

### -field dwProvSpec1

Any provider-specific data. Applications should ignore this member unless they have detailed information 
       about the format of the data required by the provider.

Set this member to <b>COMMPROP_INITIALIZED</b> before calling the 
       <a href="/windows/desktop/api/winbase/nf-winbase-getcommproperties">GetCommProperties</a> function to indicate that the 
       <b>wPacketLength</b> member is already valid.

### -field dwProvSpec2

Any provider-specific data. Applications should ignore this member unless they have detailed information 
      about the format of the data required by the provider.

### -field wcProvChar

Any provider-specific data. Applications should ignore this member unless they have detailed information 
      about the format of the data required by the provider.

## -remarks

The contents of the <b>dwProvSpec1</b>, <b>dwProvSpec2</b>, and 
    <b>wcProvChar</b> members depend on the provider subtype (specified by the 
    <b>dwProvSubType</b> member).

If the provider subtype is <b>PST_MODEM</b>, these members are used as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>dwProvSpec1</b></td>
<td>Not used.</td>
</tr>
<tr>
<td><b>dwProvSpec2</b></td>
<td>Not used.</td>
</tr>
<tr>
<td><b>wcProvChar</b></td>
<td>Contains a <a href="/windows/desktop/api/mcx/ns-mcx-modemdevcaps">MODEMDEVCAPS</a> structure.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getcommproperties">GetCommProperties</a>