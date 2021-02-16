---
UID: NS:tcpestats._TCP_ESTATS_SEND_BUFF_ROD_v0
title: TCP_ESTATS_SEND_BUFF_ROD_v0 (tcpestats.h)
description: Contains read-only dynamic information for extended TCP statistics on output queuing for a TCP connection.
helpviewer_keywords: ["*PTCP_ESTATS_SEND_BUFF_ROD_v0","PTCP_ESTATS_SEND_BUFF_ROD_v0","PTCP_ESTATS_SEND_BUFF_ROD_v0 structure pointer [IP Helper]","TCP_ESTATS_SEND_BUFF_ROD_v0","TCP_ESTATS_SEND_BUFF_ROD_v0 structure [IP Helper]","iphlp.tcp_estats_send_buff_rod_v0","tcpestats/PTCP_ESTATS_SEND_BUFF_ROD_v0","tcpestats/TCP_ESTATS_SEND_BUFF_ROD_v0"]
old-location: iphlp\tcp_estats_send_buff_rod_v0.htm
tech.root: IpHlp
ms.assetid: 7cda7378-95e4-4f1d-88b3-27974fedec83
ms.date: 12/05/2018
ms.keywords: '*PTCP_ESTATS_SEND_BUFF_ROD_v0, PTCP_ESTATS_SEND_BUFF_ROD_v0, PTCP_ESTATS_SEND_BUFF_ROD_v0 structure pointer [IP Helper], TCP_ESTATS_SEND_BUFF_ROD_v0, TCP_ESTATS_SEND_BUFF_ROD_v0 structure [IP Helper], iphlp.tcp_estats_send_buff_rod_v0, tcpestats/PTCP_ESTATS_SEND_BUFF_ROD_v0, tcpestats/TCP_ESTATS_SEND_BUFF_ROD_v0'
req.header: tcpestats.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TCP_ESTATS_SEND_BUFF_ROD_v0, *PTCP_ESTATS_SEND_BUFF_ROD_v0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_ESTATS_SEND_BUFF_ROD_v0
 - tcpestats/_TCP_ESTATS_SEND_BUFF_ROD_v0
 - PTCP_ESTATS_SEND_BUFF_ROD_v0
 - tcpestats/PTCP_ESTATS_SEND_BUFF_ROD_v0
 - TCP_ESTATS_SEND_BUFF_ROD_v0
 - tcpestats/TCP_ESTATS_SEND_BUFF_ROD_v0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpestats.h
api_name:
 - TCP_ESTATS_SEND_BUFF_ROD_v0
---

# TCP_ESTATS_SEND_BUFF_ROD_v0 structure


## -description

The <b>TCP_ESTATS_SEND_BUFF_ROD_v0</b> structure contains read-only dynamic information for extended TCP statistics on output queuing for a TCP connection.

## -struct-fields

### -field CurRetxQueue

Type: <b>SIZE_T</b>

The current number of bytes of data occupying the
           retransmit queue.

### -field MaxRetxQueue

Type: <b>SIZE_T</b>

The maximum number of bytes of data occupying the
           retransmit queue.

### -field CurAppWQueue

Type: <b>SIZE_T</b>

The current number of bytes of application data buffered
           by TCP, pending the first transmission (to the left of
           SND.NXT or SndMax).  

This data will generally be transmitted
           (and SND.NXT advanced to the left) as soon as there is an
           available congestion window or receiver window.  This is the amount of data readily available for
           transmission, without scheduling the application.  TCP
           performance may suffer if there is insufficient queued
           write data.

### -field MaxAppWQueue

Type: <b>SIZE_T</b>

The maximum number of bytes of application data buffered
           by TCP, pending the first transmission.  

This is the maximum
           value of the <b>CurAppWQueue</b> member.  The <b>MaxAppWQueue</b> and  <b>CurAppWQueue</b> members can
           be used to determine if insufficient queued data is steady
           state (suggesting insufficient queue space) or transient
           (suggesting insufficient application performance or
           excessive CPU load or scheduler latency).

## -remarks

The <b>TCP_ESTATS_SEND_BUFF_ROD_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_SEND_BUFF_ROD_v0</b> is defined as version 0 of the structure for  read-only dynamic information for extended TCP statistics on output queuing for a TCP connection.  This information is available after the connection has been established.

The <b>TCP_ESTATS_SEND_BUFF_ROD_v0</b> structure is retrieved by calls to  the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsSendBuff</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics need to be enabled to retrieve this structure.

The members of this structure are defined in the IETF RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://tools.ietf.org/html/rfc4898">http://www.ietf.org/rfc/rfc4898.txt</a>.




The following is the mapping of the members in the <b>TCP_ESTATS_SEND_BUFF_ROD_v0</b> structure to the entries defined in RFC 4898 for extended TCP statistics:



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="CurRetxQueue"></a><a id="curretxqueue"></a><a id="CURRETXQUEUE"></a><b>CurRetxQueue</b>

</td>
<td width="60%">
tcpEStatsStackCurRetxQueue

</td>
</tr>
<tr>
<td width="40%">
<a id="MaxRetxQueue"></a><a id="maxretxqueue"></a><a id="MAXRETXQUEUE"></a><b>MaxRetxQueue</b>

</td>
<td width="60%">
tcpEStatsStackMaxRetxQueue

</td>
</tr>
<tr>
<td width="40%">
<a id="CurAppWQueue"></a><a id="curappwqueue"></a><a id="CURAPPWQUEUE"></a><b>CurAppWQueue</b>

</td>
<td width="60%">
tcpEStatsAppCurAppWQueue

</td>
</tr>
<tr>
<td width="40%">
<a id="MaxAppWQueue"></a><a id="maxappwqueue"></a><a id="MAXAPPWQUEUE"></a><b>MaxAppWQueue</b>

</td>
<td width="60%">
tcpEStatsAppMaxAppWQueue

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>