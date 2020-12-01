---
UID: NS:tcpestats._TCP_ESTATS_REC_ROD_v0
title: TCP_ESTATS_REC_ROD_v0 (tcpestats.h)
description: Contains read-only dynamic information for extended TCP statistics on the local receiver for a TCP connection.
helpviewer_keywords: ["*PTCP_ESTATS_REC_ROD_v0","PTCP_ESTATS_REC_ROD_v0","PTCP_ESTATS_REC_ROD_v0 structure pointer [IP Helper]","TCP_ESTATS_REC_ROD_v0","TCP_ESTATS_REC_ROD_v0 structure [IP Helper]","iphlp.tcp_estats_rec_rod_v0","tcpestats/PTCP_ESTATS_REC_ROD_v0","tcpestats/TCP_ESTATS_REC_ROD_v0"]
old-location: iphlp\tcp_estats_rec_rod_v0.htm
tech.root: IpHlp
ms.assetid: 1481f108-1ea3-4952-9131-8b15e373d83e
ms.date: 12/05/2018
ms.keywords: '*PTCP_ESTATS_REC_ROD_v0, PTCP_ESTATS_REC_ROD_v0, PTCP_ESTATS_REC_ROD_v0 structure pointer [IP Helper], TCP_ESTATS_REC_ROD_v0, TCP_ESTATS_REC_ROD_v0 structure [IP Helper], iphlp.tcp_estats_rec_rod_v0, tcpestats/PTCP_ESTATS_REC_ROD_v0, tcpestats/TCP_ESTATS_REC_ROD_v0'
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
req.typenames: TCP_ESTATS_REC_ROD_v0, *PTCP_ESTATS_REC_ROD_v0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_ESTATS_REC_ROD_v0
 - tcpestats/_TCP_ESTATS_REC_ROD_v0
 - PTCP_ESTATS_REC_ROD_v0
 - tcpestats/PTCP_ESTATS_REC_ROD_v0
 - TCP_ESTATS_REC_ROD_v0
 - tcpestats/TCP_ESTATS_REC_ROD_v0
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
 - TCP_ESTATS_REC_ROD_v0
---

# TCP_ESTATS_REC_ROD_v0 structure


## -description

The <b>TCP_ESTATS_REC_ROD_v0</b> structure contains read-only dynamic information for extended TCP statistics on the local receiver for a TCP connection.

## -struct-fields

### -field CurRwinSent

Type: <b>ULONG</b>

The most recent window advertisement, in bytes, that has been sent.

### -field MaxRwinSent

Type: <b>ULONG</b>

The maximum window advertisement, in bytes, that has been sent.

### -field MinRwinSent

Type: <b>ULONG</b>

The minimum window advertisement, in bytes, that has been sent.

### -field LimRwin

Type: <b>ULONG</b>

The maximum window advertisement, in bytes, that may
           be sent.

### -field DupAckEpisodes

Type: <b>ULONG</b>

The number of Duplicate Acks Sent when prior Ack was not
           duplicate.  This is the number of times that a contiguous
           series of duplicate acknowledgments have been sent.

           

This is an indication of the number of data segments lost
           or reordered on the path from the remote TCP endpoint to
           the near TCP endpoint.

### -field DupAcksOut

Type: <b>ULONG</b>

The number of duplicate ACKs sent.  

The ratio of the change
           in the <b>DupAcksOut</b> member to the change in
           the <b>DupAckEpisodes</b> member  is an indication of reorder or
           recovery distance over some interval.

### -field CeRcvd

Type: <b>ULONG</b>

The number of segments received with IP headers bearing
           Congestion Experienced (CE) markings.

### -field EcnSent

Type: <b>ULONG</b>

Reserved for future use. This member is always set to zero.

### -field EcnNoncesRcvd

Type: <b>ULONG</b>

Reserved for future use. This member is always set to zero.

### -field CurReasmQueue

Type: <b>ULONG</b>

The current number of bytes of sequence space spanned by
           the reassembly queue.

This is generally the difference
           between rcv.nxt and the sequence number of the right most
           edge of the reassembly queue.

### -field MaxReasmQueue

Type: <b>ULONG</b>

The maximum number of bytes of sequence space spanned by
           the reassembly queue. 

This is the maximum value of the <b>CurReasmQueue</b> member.

### -field CurAppRQueue

Type: <b>SIZE_T</b>

The current number of bytes of application data that has
           been acknowledged by TCP but not yet delivered to the
           application.

### -field MaxAppRQueue

Type: <b>SIZE_T</b>

The maximum number of bytes of application data that has
           been acknowledged by TCP but not yet delivered to the
           application.

### -field WinScaleSent

Type: <b>UCHAR</b>

The value of the transmitted window scale option if one was
           sent; otherwise, a value of -1.

Note that if both the <b>WinScaleSent</b> member and
           the <b>WinScaleRcvd</b> member of the <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_obs_rec_rod_v0">TCP_ESTATS_OBS_REC_ROD_v0</a> structure are not -1, then Rcv.Wind.Scale
           will be the same as this value and used to scale receiver
           window announcements from the local host to the remote
           host.

## -remarks

The <b>TCP_ESTATS_REC_ROD_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_REC_ROD_v0</b> is defined as version 0 of the structure for  read-only dynamic information for extended TCP statistics on the local receiver for a TCP connection.  This information is available after the connection has been established.

The <b>TCP_ESTATS_REC_ROD_v0</b> structure is retrieved by calls to  the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsRec</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics need to be enabled to retrieve this structure.

TCP congestion control and congestion control algorithms are discussed in detail in the IETF RFC 2581 on TCP Congestion Control. For more information, see <a href="http://tools.ietf.org/html/rfc2581">http://www.ietf.org/rfc/rfc2581.txt</a>.

Explicit Congestion Notification in IP is discussed in detail in the IETF RFC 2581 on The Addition of Explicit Congestion Notification
           (ECN) to IP. For more information, see <a href="http://tools.ietf.org/html/rfc3168">http://www.ietf.org/rfc/rfc3168.txt</a>.

The members of this structure are defined in the IETF RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://tools.ietf.org/html/rfc4898">http://www.ietf.org/rfc/rfc4898.txt</a>.




The following is the mapping of the members in the <b>TCP_ESTATS_REC_ROD_v0</b> structure to the entries defined in RFC 4898 for extended TCP statistics:



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="CurRwinSent"></a><a id="currwinsent"></a><a id="CURRWINSENT"></a><b>CurRwinSent</b>

</td>
<td width="60%">
tcpEStatsPerfCurRwinSent

</td>
</tr>
<tr>
<td width="40%">
<a id="MaxRwinSent"></a><a id="maxrwinsent"></a><a id="MAXRWINSENT"></a><b>MaxRwinSent</b>

</td>
<td width="60%">
tcpEStatsPerfMaxRwinSent

</td>
</tr>
<tr>
<td width="40%">
<a id="MinRwinSent"></a><a id="minrwinsent"></a><a id="MINRWINSENT"></a><b>MinRwinSent</b>

</td>
<td width="60%">
No mapping to this member.

</td>
</tr>
<tr>
<td width="40%">
<a id="LimRwin"></a><a id="limrwin"></a><a id="LIMRWIN"></a><b>LimRwin</b>

</td>
<td width="60%">
tcpEStatsTuneLimRwin

</td>
</tr>
<tr>
<td width="40%">
<a id="DupAckEpisodes"></a><a id="dupackepisodes"></a><a id="DUPACKEPISODES"></a><b>DupAckEpisodes</b>

</td>
<td width="60%">
tcpEStatsPathDupAckEpisodes

</td>
</tr>
<tr>
<td width="40%">
<a id="DupAcksOut"></a><a id="dupacksout"></a><a id="DUPACKSOUT"></a><b>DupAcksOut</b>

</td>
<td width="60%">
tcpEStatsPathDupAcksOut

</td>
</tr>
<tr>
<td width="40%">
<a id="CeRcvd"></a><a id="cercvd"></a><a id="CERCVD"></a><b>CeRcvd</b>

</td>
<td width="60%">
tcpEStatsPathCERcvd

</td>
</tr>
<tr>
<td width="40%">
<a id="EcnSent"></a><a id="ecnsent"></a><a id="ECNSENT"></a><b>EcnSent</b>

</td>
<td width="60%">
No mapping to this member.

</td>
</tr>
<tr>
<td width="40%">
<a id="EcnNoncesRcvd"></a><a id="ecnnoncesrcvd"></a><a id="ECNNONCESRCVD"></a><b>EcnNoncesRcvd</b>

</td>
<td width="60%">
No mapping to this member.

</td>
</tr>
<tr>
<td width="40%">
<a id="CurReasmQueue"></a><a id="curreasmqueue"></a><a id="CURREASMQUEUE"></a><b>CurReasmQueue</b>

</td>
<td width="60%">
tcpEStatsStackCurReasmQueue

</td>
</tr>
<tr>
<td width="40%">
<a id="MaxReasmQueue"></a><a id="maxreasmqueue"></a><a id="MAXREASMQUEUE"></a><b>MaxReasmQueue</b>

</td>
<td width="60%">
tcpEStatsStackMaxReasmQueue

</td>
</tr>
<tr>
<td width="40%">
<a id="CurAppRQueue"></a><a id="curapprqueue"></a><a id="CURAPPRQUEUE"></a><b>CurAppRQueue</b>

</td>
<td width="60%">
tcpEStatsAppCurAppRQueue

</td>
</tr>
<tr>
<td width="40%">
<a id="MaxAppRQueue"></a><a id="maxapprqueue"></a><a id="MAXAPPRQUEUE"></a><b>MaxAppRQueue</b>

</td>
<td width="60%">
tcpEStatsAppMaxAppRQueue

</td>
</tr>
<tr>
<td width="40%">
<a id="WinScaleSent"></a><a id="winscalesent"></a><a id="WINSCALESENT"></a><b>WinScaleSent</b>

</td>
<td width="60%">
tcpEStatsStackWinScaleSent

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>