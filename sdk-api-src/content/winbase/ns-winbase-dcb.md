---
UID: NS:winbase._DCB
title: DCB (winbase.h)
description: Defines the control setting for a serial communications device.
helpviewer_keywords: ["*LPDCB","CBR_110","CBR_115200","CBR_1200","CBR_128000","CBR_14400","CBR_19200","CBR_2400","CBR_256000","CBR_300","CBR_38400","CBR_4800","CBR_57600","CBR_600","CBR_9600","DCB","DCB structure","DTR_CONTROL_DISABLE","DTR_CONTROL_ENABLE","DTR_CONTROL_HANDSHAKE","EVENPARITY","LPDCB","LPDCB structure pointer","MARKPARITY","NOPARITY","ODDPARITY","ONE5STOPBITS","ONESTOPBIT","RTS_CONTROL_DISABLE","RTS_CONTROL_ENABLE","RTS_CONTROL_HANDSHAKE","RTS_CONTROL_TOGGLE","SPACEPARITY","TWOSTOPBITS","_DCB","_win32_dcb_str","base.dcb_str","winbase/DCB","winbase/LPDCB"]
old-location: base\dcb_str.htm
tech.root: base
ms.assetid: 9dccd2c6-44b7-4609-a2b9-9815430bf3c7
ms.date: 12/05/2018
ms.keywords: '*LPDCB, CBR_110, CBR_115200, CBR_1200, CBR_128000, CBR_14400, CBR_19200, CBR_2400, CBR_256000, CBR_300, CBR_38400, CBR_4800, CBR_57600, CBR_600, CBR_9600, DCB, DCB structure, DTR_CONTROL_DISABLE, DTR_CONTROL_ENABLE, DTR_CONTROL_HANDSHAKE, EVENPARITY, LPDCB, LPDCB structure pointer, MARKPARITY, NOPARITY, ODDPARITY, ONE5STOPBITS, ONESTOPBIT, RTS_CONTROL_DISABLE, RTS_CONTROL_ENABLE, RTS_CONTROL_HANDSHAKE, RTS_CONTROL_TOGGLE, SPACEPARITY, TWOSTOPBITS, _DCB, _win32_dcb_str, base.dcb_str, winbase/DCB, winbase/LPDCB'
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
req.typenames: DCB, *LPDCB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DCB
 - winbase/_DCB
 - LPDCB
 - winbase/LPDCB
 - DCB
 - winbase/DCB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - DCB
---

# DCB structure


## -description

Defines the control setting for a serial communications device.

## -struct-fields

### -field DCBlength

The length of the structure, in bytes. The caller must set this member to 
      <code>sizeof(DCB)</code>.

### -field BaudRate

The baud rate at which the communications device operates. This member can be an actual baud rate value, or 
      one of the following indexes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CBR_110"></a><a id="cbr_110"></a><dl>
<dt><b>CBR_110</b></dt>
<dt>110</dt>
</dl>
</td>
<td width="60%">
110 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_300"></a><a id="cbr_300"></a><dl>
<dt><b>CBR_300</b></dt>
<dt>300</dt>
</dl>
</td>
<td width="60%">
300 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_600"></a><a id="cbr_600"></a><dl>
<dt><b>CBR_600</b></dt>
<dt>600</dt>
</dl>
</td>
<td width="60%">
600 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_1200"></a><a id="cbr_1200"></a><dl>
<dt><b>CBR_1200</b></dt>
<dt>1200</dt>
</dl>
</td>
<td width="60%">
1200 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_2400"></a><a id="cbr_2400"></a><dl>
<dt><b>CBR_2400</b></dt>
<dt>2400</dt>
</dl>
</td>
<td width="60%">
2400 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_4800"></a><a id="cbr_4800"></a><dl>
<dt><b>CBR_4800</b></dt>
<dt>4800</dt>
</dl>
</td>
<td width="60%">
4800 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_9600"></a><a id="cbr_9600"></a><dl>
<dt><b>CBR_9600</b></dt>
<dt>9600</dt>
</dl>
</td>
<td width="60%">
9600 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_14400"></a><a id="cbr_14400"></a><dl>
<dt><b>CBR_14400</b></dt>
<dt>14400</dt>
</dl>
</td>
<td width="60%">
14400 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_19200"></a><a id="cbr_19200"></a><dl>
<dt><b>CBR_19200</b></dt>
<dt>19200</dt>
</dl>
</td>
<td width="60%">
19200 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_38400"></a><a id="cbr_38400"></a><dl>
<dt><b>CBR_38400</b></dt>
<dt>38400</dt>
</dl>
</td>
<td width="60%">
 38400 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_57600"></a><a id="cbr_57600"></a><dl>
<dt><b>CBR_57600</b></dt>
<dt>57600</dt>
</dl>
</td>
<td width="60%">
57600 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_115200"></a><a id="cbr_115200"></a><dl>
<dt><b>CBR_115200</b></dt>
<dt>115200</dt>
</dl>
</td>
<td width="60%">
115200 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_128000"></a><a id="cbr_128000"></a><dl>
<dt><b>CBR_128000</b></dt>
<dt>128000</dt>
</dl>
</td>
<td width="60%">
128000 bps

</td>
</tr>
<tr>
<td width="40%"><a id="CBR_256000"></a><a id="cbr_256000"></a><dl>
<dt><b>CBR_256000</b></dt>
<dt>256000</dt>
</dl>
</td>
<td width="60%">
256000 bps

</td>
</tr>
</table>

### -field fBinary

If this member is <b>TRUE</b>, binary mode is enabled. Windows does not support 
      nonbinary mode transfers, so this member must be <b>TRUE</b>.

### -field fParity

If this member is <b>TRUE</b>, parity checking is performed and errors are 
      reported.

### -field fOutxCtsFlow

If this member is <b>TRUE</b>, the CTS (clear-to-send) signal is monitored for output 
      flow control. If this member is <b>TRUE</b> and CTS is turned off, output is suspended until 
      CTS is sent again.

### -field fOutxDsrFlow

If this member is <b>TRUE</b>, the DSR (data-set-ready) signal is monitored for output 
      flow control. If this member is <b>TRUE</b> and DSR is turned off, output is suspended until 
      DSR is sent again.

### -field fDtrControl

The DTR (data-terminal-ready) flow control. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DTR_CONTROL_DISABLE"></a><a id="dtr_control_disable"></a><dl>
<dt><b>DTR_CONTROL_DISABLE</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Disables the DTR line when the device is opened and leaves it disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="DTR_CONTROL_ENABLE"></a><a id="dtr_control_enable"></a><dl>
<dt><b>DTR_CONTROL_ENABLE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Enables the DTR line when the device is opened and leaves it on.

</td>
</tr>
<tr>
<td width="40%"><a id="DTR_CONTROL_HANDSHAKE"></a><a id="dtr_control_handshake"></a><dl>
<dt><b>DTR_CONTROL_HANDSHAKE</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Enables DTR handshaking. If handshaking is enabled, it is an error for the application to adjust the line 
        by using the <a href="/windows/desktop/api/winbase/nf-winbase-escapecommfunction">EscapeCommFunction</a> function.

</td>
</tr>
</table>

### -field fDsrSensitivity

If this member is <b>TRUE</b>, the communications driver is sensitive to the state of 
      the DSR signal. The driver ignores any bytes received, unless the DSR modem input line is high.

### -field fTXContinueOnXoff

If this member is <b>TRUE</b>, transmission continues after the input buffer has come 
      within <b>XoffLim</b> bytes of being full and the driver has transmitted the 
      <b>XoffChar</b> character to stop receiving bytes. If this member is 
      <b>FALSE</b>, transmission does not continue until the input buffer is within 
      <b>XonLim</b> bytes of being empty and the driver has transmitted 
      the <b>XonChar</b> character to resume reception.

### -field fOutX

Indicates whether XON/XOFF flow control is used during transmission. If this member is 
      <b>TRUE</b>, transmission stops when the <b>XoffChar</b> character is 
      received and starts again when the <b>XonChar</b> character is received.

### -field fInX

Indicates whether XON/XOFF flow control is used during reception. If this member is 
      <b>TRUE</b>, the <b>XoffChar</b> character is sent when the input buffer 
      comes within <b>XoffLim</b> bytes of being full, and the <b>XonChar</b> 
      character is sent when the input buffer comes within <b>XonLim</b> bytes of being 
      empty.

### -field fErrorChar

Indicates whether bytes received with parity errors are replaced with the character specified by the 
      <b>ErrorChar</b> member. If this member is <b>TRUE</b> and the 
      <b>fParity</b> member is <b>TRUE</b>, replacement occurs.

### -field fNull

If this member is <b>TRUE</b>, null bytes are discarded when received.

### -field fRtsControl

The RTS (request-to-send) flow control. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTS_CONTROL_DISABLE"></a><a id="rts_control_disable"></a><dl>
<dt><b>RTS_CONTROL_DISABLE</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Disables the RTS line when the device is opened and leaves it disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="RTS_CONTROL_ENABLE"></a><a id="rts_control_enable"></a><dl>
<dt><b>RTS_CONTROL_ENABLE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Enables the RTS line when the device is opened and leaves it on.

</td>
</tr>
<tr>
<td width="40%"><a id="RTS_CONTROL_HANDSHAKE"></a><a id="rts_control_handshake"></a><dl>
<dt><b>RTS_CONTROL_HANDSHAKE</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Enables RTS handshaking. The driver raises the RTS line when the "type-ahead" (input) buffer is less than 
        one-half full and lowers the RTS line when the buffer is more than three-quarters full. If handshaking is 
        enabled, it is an error for the application to adjust the line by using the 
        <a href="/windows/desktop/api/winbase/nf-winbase-escapecommfunction">EscapeCommFunction</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="RTS_CONTROL_TOGGLE"></a><a id="rts_control_toggle"></a><dl>
<dt><b>RTS_CONTROL_TOGGLE</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
Specifies that the RTS line will be high if bytes are available for transmission. After all buffered 
        bytes have been sent, the RTS line will be low.

</td>
</tr>
</table>

### -field fAbortOnError

If this member is <b>TRUE</b>, the driver terminates all read and write operations with 
      an error status if an error occurs. The driver will not accept any further communications operations until the 
      application has acknowledged the error by calling the 
      <a href="/windows/desktop/api/winbase/nf-winbase-clearcommerror">ClearCommError</a> function.

### -field fDummy2

Reserved; do not use.

### -field wReserved

Reserved; must be zero.

### -field XonLim

The minimum number of bytes in use allowed in the input buffer before flow control is activated to allow 
      transmission by the sender. This assumes that either XON/XOFF, RTS, or DTR input flow control is specified in 
      the <b>fInX</b>, <b>fRtsControl</b>, or 
      <b>fDtrControl</b> members.

### -field XoffLim

The minimum number of free bytes allowed in the input buffer before flow control is activated to inhibit 
      the sender. Note that the sender may transmit characters after the flow control signal has been activated, so 
      this value should never be zero. This assumes that either XON/XOFF, RTS, or DTR input flow control is specified 
      in the <b>fInX</b>, <b>fRtsControl</b>, or 
      <b>fDtrControl</b> members. The maximum number of bytes in use allowed is calculated by 
      subtracting this value from the size, in bytes, of the input buffer.

### -field ByteSize

The number of bits in the bytes transmitted and received.

### -field Parity

The parity scheme to be used. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENPARITY"></a><a id="evenparity"></a><dl>
<dt><b>EVENPARITY</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Even parity.

</td>
</tr>
<tr>
<td width="40%"><a id="MARKPARITY"></a><a id="markparity"></a><dl>
<dt><b>MARKPARITY</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Mark parity.

</td>
</tr>
<tr>
<td width="40%"><a id="NOPARITY"></a><a id="noparity"></a><dl>
<dt><b>NOPARITY</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No parity.

</td>
</tr>
<tr>
<td width="40%"><a id="ODDPARITY"></a><a id="oddparity"></a><dl>
<dt><b>ODDPARITY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Odd parity.

</td>
</tr>
<tr>
<td width="40%"><a id="SPACEPARITY"></a><a id="spaceparity"></a><dl>
<dt><b>SPACEPARITY</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Space parity.

</td>
</tr>
</table>

### -field StopBits

The number of stop bits to be used. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ONESTOPBIT"></a><a id="onestopbit"></a><dl>
<dt><b>ONESTOPBIT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
1 stop bit.

</td>
</tr>
<tr>
<td width="40%"><a id="ONE5STOPBITS"></a><a id="one5stopbits"></a><dl>
<dt><b>ONE5STOPBITS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
1.5 stop bits.

</td>
</tr>
<tr>
<td width="40%"><a id="TWOSTOPBITS"></a><a id="twostopbits"></a><dl>
<dt><b>TWOSTOPBITS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
2 stop bits.

</td>
</tr>
</table>

### -field XonChar

The value of the XON character for both transmission and reception.

### -field XoffChar

The value of the XOFF character for both transmission and reception.

### -field ErrorChar

The value of the character used to replace bytes received with a parity error.

### -field EofChar

The value of the character used to signal the end of data.

### -field EvtChar

The value of the character used to signal an event.

### -field wReserved1

Reserved; do not use.

## -remarks

When a <b>DCB</b> structure is used to configure the 8250, the 
    following restrictions apply to the values specified for the <b>ByteSize</b> and 
    <b>StopBits</b> members:

<ul>
<li>The number of data bits must be 5 to 8 bits.</li>
<li>The use of 5 data bits with 2 stop bits is an invalid combination, as is 6, 7, or 8 data bits with 1.5 stop 
      bits.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-buildcommdcba">BuildCommDCB</a>



<a href="/windows/desktop/api/winbase/nf-winbase-clearcommerror">ClearCommError</a>



<a href="/windows/desktop/api/winbase/nf-winbase-escapecommfunction">EscapeCommFunction</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getcommstate">GetCommState</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommstate">SetCommState</a>