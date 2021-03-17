---
UID: NS:mswsock._TRANSMIT_PACKETS_ELEMENT
title: TRANSMIT_PACKETS_ELEMENT (mswsock.h)
description: Specifies a single data element to be transmitted by the TransmitPackets function.
helpviewer_keywords: ["*LPTRANSMIT_PACKETS_ELEMENT","*PTRANSMIT_PACKETS_ELEMENT","TP_ELEMENT_EOP","TP_ELEMENT_FILE","TP_ELEMENT_MEMORY","TRANSMIT_PACKETS_ELEMENT","TRANSMIT_PACKETS_ELEMENT structure [Winsock]","_win32_transmit_packets_element_2","mswsock/TRANSMIT_PACKETS_ELEMENT","winsock.transmit_packets_element_2"]
old-location: winsock\transmit_packets_element_2.htm
tech.root: WinSock
ms.assetid: cf9f8cd1-284d-4aed-bb43-af02bd012f01
ms.date: 12/05/2018
ms.keywords: '*LPTRANSMIT_PACKETS_ELEMENT, *PTRANSMIT_PACKETS_ELEMENT, TP_ELEMENT_EOP, TP_ELEMENT_FILE, TP_ELEMENT_MEMORY, TRANSMIT_PACKETS_ELEMENT, TRANSMIT_PACKETS_ELEMENT structure [Winsock], _win32_transmit_packets_element_2, mswsock/TRANSMIT_PACKETS_ELEMENT, winsock.transmit_packets_element_2'
req.header: mswsock.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: TRANSMIT_PACKETS_ELEMENT, *PTRANSMIT_PACKETS_ELEMENT, *LPTRANSMIT_PACKETS_ELEMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRANSMIT_PACKETS_ELEMENT
 - mswsock/_TRANSMIT_PACKETS_ELEMENT
 - PTRANSMIT_PACKETS_ELEMENT
 - mswsock/PTRANSMIT_PACKETS_ELEMENT
 - TRANSMIT_PACKETS_ELEMENT
 - mswsock/TRANSMIT_PACKETS_ELEMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mswsock.h
api_name:
 - TRANSMIT_PACKETS_ELEMENT
---

# TRANSMIT_PACKETS_ELEMENT structure


## -description

The 
<b>TRANSMIT_PACKETS_ELEMENT</b> structure specifies a single data element to be transmitted by the 
<a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_transmitpackets">TransmitPackets</a> function.

## -struct-fields

### -field dwElFlags

Type: <b>ULONG</b>

Flags used to describe the contents of the packet array element, and to customize 
<b>TransmitPackets</b> function processing. The following table lists valid flags:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TP_ELEMENT_FILE"></a><a id="tp_element_file"></a><dl>
<dt><b>TP_ELEMENT_FILE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that data resides in a file. Default setting for <b>dwElFlags</b>. Mutually exclusive with TP_ELEMENT_MEMORY.

</td>
</tr>
<tr>
<td width="40%"><a id="TP_ELEMENT_MEMORY"></a><a id="tp_element_memory"></a><dl>
<dt><b>TP_ELEMENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Specifies that data resides in memory. Mutually exclusive with TP_ELEMENT_FILE.

</td>
</tr>
<tr>
<td width="40%"><a id="TP_ELEMENT_EOP"></a><a id="tp_element_eop"></a><dl>
<dt><b>TP_ELEMENT_EOP</b></dt>
</dl>
</td>
<td width="60%">
Specifies that this element should not be combined with the next element in a single 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> request from the sockets layer to the transport. This flag is used for granular control of the content of each message on a datagram or message-oriented socket.

</td>
</tr>
</table>

### -field cLength

Type: <b>ULONG</b>

The number of bytes to transmit. If zero, the entire file is transmitted.

### -field nFileOffset

Type: <b>LARGE_INTEGER</b>

The file offset, in bytes, at which to begin the transfer. Valid only if TP_ELEMENT_FILE is specified in <b>dwEIFlags</b>. When set to –1, transmission begins at the current byte offset.

### -field hFile

Type: <b>HANDLE</b>

A handle to an open file to be transmitted. Valid only if TP_ELEMENT_FILE is specified in <b>dwEIFlags</b>. Windows reads the file sequentially; caching performance is improved by opening this handle with FILE_FLAG_SEQUENTIAL_SCAN.

### -field pBuffer

Type: <b>PVOID</b>

A pointer to the data in memory to be sent. Valid only if TP_ELEMENT_MEMORY is specified in <b>dwEIFlags</b>.

## -see-also

<a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_transmitpackets">TransmitPackets</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a>



<b>send</b>