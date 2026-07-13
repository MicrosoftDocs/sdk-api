---
UID: NS:nspapi._PROTOCOL_INFOA
title: PROTOCOL_INFOA (nspapi.h)
description: Contains information about a protocol. (ANSI)
helpviewer_keywords: ["*LPPROTOCOL_INFOA","*PPROTOCOL_INFOA","0","0xFFFFFFFF","PROTOCOL_INFO","PROTOCOL_INFO structure [Winsock]","PROTOCOL_INFOA","PROTOCOL_INFOW","XP_BANDWIDTH_ALLOCATION","XP_CONNECTIONLESS","XP_CONNECT_DATA","XP_DISCONNECT_DATA","XP_ENCRYPTS","XP_EXPEDITED_DATA","XP_FRAGMENTATION","XP_GRACEFUL_CLOSE","XP_GUARANTEED_DELIVERY","XP_GUARANTEED_ORDER","XP_MESSAGE_ORIENTED","XP_PSEUDO_STREAM","XP_SUPPORTS_BROADCAST","XP_SUPPORTS_MULTICAST","_win32_protocol_info_2","nspapi/PROTOCOL_INFO","nspapi/PROTOCOL_INFOA","nspapi/PROTOCOL_INFOW","winsock.protocol_info_2"]
old-location: winsock\protocol_info_2.htm
tech.root: WinSock
ms.assetid: 0cbddf17-41a8-4e61-b3b0-080ef50dc5de
ms.date: 12/05/2018
ms.keywords: '*LPPROTOCOL_INFOA, *PPROTOCOL_INFOA, 0, 0xFFFFFFFF, PROTOCOL_INFO, PROTOCOL_INFO structure [Winsock], PROTOCOL_INFOA, PROTOCOL_INFOW, XP_BANDWIDTH_ALLOCATION, XP_CONNECTIONLESS, XP_CONNECT_DATA, XP_DISCONNECT_DATA, XP_ENCRYPTS, XP_EXPEDITED_DATA, XP_FRAGMENTATION, XP_GRACEFUL_CLOSE, XP_GUARANTEED_DELIVERY, XP_GUARANTEED_ORDER, XP_MESSAGE_ORIENTED, XP_PSEUDO_STREAM, XP_SUPPORTS_BROADCAST, XP_SUPPORTS_MULTICAST, _win32_protocol_info_2, nspapi/PROTOCOL_INFO, nspapi/PROTOCOL_INFOA, nspapi/PROTOCOL_INFOW, winsock.protocol_info_2'
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PROTOCOL_INFOW (Unicode) and PROTOCOL_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROTOCOL_INFOA, *PPROTOCOL_INFOA, *LPPROTOCOL_INFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROTOCOL_INFOA
 - nspapi/_PROTOCOL_INFOA
 - PPROTOCOL_INFOA
 - nspapi/PPROTOCOL_INFOA
 - PROTOCOL_INFOA
 - nspapi/PROTOCOL_INFOA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nspapi.h
api_name:
 - PROTOCOL_INFO
 - PROTOCOL_INFOA
 - PROTOCOL_INFOW
---

# PROTOCOL_INFOA structure


## -description

The 
<b>PROTOCOL_INFO</b> structure contains information about a protocol.

## -struct-fields

### -field dwServiceFlags

Type: <b>DWORD</b>

A set of bit flags that specifies the services provided by the protocol. One or more of the following bit flags may be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XP_CONNECTIONLESS"></a><a id="xp_connectionless"></a><dl>
<dt><b>XP_CONNECTIONLESS</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol provides connectionless (datagram) service. If this flag is clear, the protocol provides connection-oriented data transfer.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_GUARANTEED_DELIVERY"></a><a id="xp_guaranteed_delivery"></a><dl>
<dt><b>XP_GUARANTEED_DELIVERY</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol guarantees that all data sent will reach the intended destination. If this flag is clear, there is no such guarantee.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_GUARANTEED_ORDER"></a><a id="xp_guaranteed_order"></a><dl>
<dt><b>XP_GUARANTEED_ORDER</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol guarantees that data will arrive in the order in which it was sent. Note that this characteristic does not guarantee delivery of the data, only its order. If this flag is clear, the order of data sent is not guaranteed.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_MESSAGE_ORIENTED"></a><a id="xp_message_oriented"></a><dl>
<dt><b>XP_MESSAGE_ORIENTED</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol is message-oriented. A message-oriented protocol honors message boundaries. If this flag is clear, the protocol is stream oriented, and the concept of message boundaries is irrelevant.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_PSEUDO_STREAM"></a><a id="xp_pseudo_stream"></a><dl>
<dt><b>XP_PSEUDO_STREAM</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol is a message-oriented protocol that ignores message boundaries for all receive operations. 




This optional capability is useful when you do not want the protocol to frame messages. An application that requires stream-oriented characteristics can open a socket with type SOCK_STREAM for transport protocols that support this functionality, regardless of the value of <b>iSocketType</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_GRACEFUL_CLOSE"></a><a id="xp_graceful_close"></a><dl>
<dt><b>XP_GRACEFUL_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol supports two-phase close operations, also known as graceful close operations. If this flag is clear, the protocol supports only abortive close operations.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_EXPEDITED_DATA"></a><a id="xp_expedited_data"></a><dl>
<dt><b>XP_EXPEDITED_DATA</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol supports expedited data, also known as urgent data.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_CONNECT_DATA"></a><a id="xp_connect_data"></a><dl>
<dt><b>XP_CONNECT_DATA</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol supports connect data.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_DISCONNECT_DATA"></a><a id="xp_disconnect_data"></a><dl>
<dt><b>XP_DISCONNECT_DATA</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol supports disconnect data.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_SUPPORTS_BROADCAST"></a><a id="xp_supports_broadcast"></a><dl>
<dt><b>XP_SUPPORTS_BROADCAST</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol supports a broadcast mechanism.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_SUPPORTS_MULTICAST"></a><a id="xp_supports_multicast"></a><dl>
<dt><b>XP_SUPPORTS_MULTICAST</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol supports a multicast mechanism.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_BANDWIDTH_ALLOCATION"></a><a id="xp_bandwidth_allocation"></a><dl>
<dt><b>XP_BANDWIDTH_ALLOCATION</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol supports a mechanism for allocating a guaranteed bandwidth to an application.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_FRAGMENTATION"></a><a id="xp_fragmentation"></a><dl>
<dt><b>XP_FRAGMENTATION</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol supports message fragmentation; physical network MTU is hidden from applications.

</td>
</tr>
<tr>
<td width="40%"><a id="XP_ENCRYPTS"></a><a id="xp_encrypts"></a><dl>
<dt><b>XP_ENCRYPTS</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the protocol supports data encryption.

</td>
</tr>
</table>

### -field iAddressFamily

Type: <b>INT</b>

Value to pass as the <i>af</i> parameter when the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> function is called to open a socket for the protocol. This address family value uniquely defines the structure of protocol addresses, also known as 
<b>sockaddr</b> structures, used by the protocol.

### -field iMaxSockAddr

Type: <b>INT</b>

Maximum length of a socket address supported by the protocol, in bytes.

### -field iMinSockAddr

Type: <b>INT</b>

Minimum length of a socket address supported by the protocol, in bytes.

### -field iSocketType

Type: <b>INT</b>

Value to pass as the <i>type</i> parameter when the 
<b>socket</b> function is called to open a socket for the protocol. 




Note that if XP_PSEUDO_STREAM is set in <b>dwServiceFlags</b>, the application can specify SOCK_STREAM as the <i>type</i> parameter to 
<b>socket</b>, regardless of the value of <b>iSocketType</b>.

### -field iProtocol

Type: <b>INT</b>

Value to pass as the <i>protocol</i> parameter when the 
<b>socket</b> function is called to open a socket for the protocol.

### -field dwMessageSize

Type: <b>DWORD</b>

Maximum message size supported by the protocol, in bytes. This is the maximum size of a message that can be sent from or received by the host. For protocols that do not support message framing, the actual maximum size of a message that can be sent to a given address may be less than this value. 




The following special message size values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The protocol is stream-oriented; the concept of message size is not relevant.

</td>
</tr>
<tr>
<td width="40%"><a id="0xFFFFFFFF"></a><a id="0xffffffff"></a><a id="0XFFFFFFFF"></a><dl>
<dt><b>0xFFFFFFFF</b></dt>
</dl>
</td>
<td width="60%">
The protocol is message-oriented, but there is no maximum message size.

</td>
</tr>
</table>

### -field lpProtocol

Type: <b>LPTSTR</b>

Pointer to a zero-terminated string that supplies a name for the protocol; for example, "SPX2."

## -see-also

<a href="/windows/desktop/api/nspapi/nf-nspapi-enumprotocolsa">EnumProtocols</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>

## -remarks

> [!NOTE]
> The nspapi.h header defines PROTOCOL_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
