---
UID: NS:tcpestats._TCP_ESTATS_DATA_ROD_v0
title: TCP_ESTATS_DATA_ROD_v0 (tcpestats.h)
description: Contains read-only dynamic information for extended TCP statistics on data transfer for a TCP connection.
helpviewer_keywords: ["*PTCP_ESTATS_DATA_ROD_v0","PTCP_ESTATS_DATA_ROD_v0","PTCP_ESTATS_DATA_ROD_v0 structure pointer [IP Helper]","TCP_ESTATS_DATA_ROD_v0","TCP_ESTATS_DATA_ROD_v0 structure [IP Helper]","iphlp.tcp_estats_data_rod_v0","tcpestats/PTCP_ESTATS_DATA_ROD_v0","tcpestats/TCP_ESTATS_DATA_ROD_v0"]
old-location: iphlp\tcp_estats_data_rod_v0.htm
tech.root: IpHlp
ms.assetid: 1e896660-10dd-471a-b4ae-116caa7a9d48
ms.date: 12/05/2018
ms.keywords: '*PTCP_ESTATS_DATA_ROD_v0, PTCP_ESTATS_DATA_ROD_v0, PTCP_ESTATS_DATA_ROD_v0 structure pointer [IP Helper], TCP_ESTATS_DATA_ROD_v0, TCP_ESTATS_DATA_ROD_v0 structure [IP Helper], iphlp.tcp_estats_data_rod_v0, tcpestats/PTCP_ESTATS_DATA_ROD_v0, tcpestats/TCP_ESTATS_DATA_ROD_v0'
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
req.typenames: TCP_ESTATS_DATA_ROD_v0, *PTCP_ESTATS_DATA_ROD_v0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_ESTATS_DATA_ROD_v0
 - tcpestats/_TCP_ESTATS_DATA_ROD_v0
 - PTCP_ESTATS_DATA_ROD_v0
 - tcpestats/PTCP_ESTATS_DATA_ROD_v0
 - TCP_ESTATS_DATA_ROD_v0
 - tcpestats/TCP_ESTATS_DATA_ROD_v0
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
 - TCP_ESTATS_DATA_ROD_v0
---

# TCP_ESTATS_DATA_ROD_v0 structure


## -description

The <b>TCP_ESTATS_DATA_ROD_v0</b> structure contains read-only dynamic information for extended TCP statistics on data transfer for a TCP connection.

## -struct-fields

### -field DataBytesOut

Type: <b>ULONG64</b>

The number of octets of data contained in transmitted
           segments, including retransmitted data.  Note that this does
           not include TCP headers.

### -field DataSegsOut

Type: <b>ULONG64</b>

The number of segments sent containing a positive length
           data segment.

### -field DataBytesIn

Type: <b>ULONG64</b>

The number of octets contained in received data segments,
           including retransmitted data.  Note that this does not
           include TCP headers.

### -field DataSegsIn

Type: <b>ULONG64</b>

The number of segments received containing a positive
 length data segment.

### -field SegsOut

Type: <b>ULONG64</b>

The total number of segments sent.

### -field SegsIn

Type: <b></b>

The total number of segments received.

### -field SoftErrors

Type: <b>ULONG</b>

The number of segments that fail various consistency tests
           during TCP input processing.  Soft errors might cause the
           segment to be discarded but some do not.  Some of these soft
           errors cause the generation of a TCP acknowledgment, while
           others are silently discarded.

### -field SoftErrorReason

Type: <b>ULONG</b>

A value that identifies which consistency test most recently
           failed during TCP input processing.  This object is set every time the <b>SoftErrors</b> member is incremented.

### -field SndUna

Type: <b>ULONG</b>

The value of the oldest unacknowledged sequence
           number. Note that this member is a TCP state variable.

### -field SndNxt

Type: <b>ULONG</b>

The next sequence number to be sent.
           Note that this member is not monotonic (and thus not
           a counter), because TCP sometimes retransmits lost data by
           pulling the member back to the missing data.

### -field SndMax

Type: <b>ULONG</b>

The farthest forward (right most or largest) sequence number to be sent.
           Note that this will be equal to the <b>SndNxt</b> member except
           when the <b>SndNxt</b> member is pulled back during recovery.

### -field ThruBytesAcked

Type: <b>ULONG64</b>

The number of octets for which cumulative acknowledgments
           have been received.  Note that this will be the sum of
           changes to the <b>SndNxt</b> member.

### -field RcvNxt

Type: <b>ULONG</b>

The next sequence number to be received.
           Note that this member is not monotonic (and thus not
           a counter), because TCP sometimes retransmits lost data by
           pulling the member back to the missing data.

### -field ThruBytesReceived

Type: <b>ULONG64</b>

The number of octets for which cumulative acknowledgments
           have been sent.  Note that this will be the sum of changes
           to the <b>RcvNxt</b> member.

## -remarks

The <b>TCP_ESTATS_DATA_ROD_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_DATA_ROD_v0</b> is defined as version 0 of the structure for  read-only dynamic information for extended TCP statistics on data transfer for a TCP connection.  This information is available after the connection has been established.

The <b>TCP_ESTATS_DATA_ROD_v0</b> structure is retrieved by calls to  the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsData</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics need to be enabled to retrieve this structure.

The members of this structure are defined in the IETF RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://tools.ietf.org/html/rfc4898">http://www.ietf.org/rfc/rfc4898.txt</a>.




The following is the mapping of the members in the <b>TCP_ESTATS_DATA_ROD_v0</b> structure to the entries defined in RFC 4898 for extended TCP statistics:



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="DataBytesOut"></a><a id="databytesout"></a><a id="DATABYTESOUT"></a><b>DataBytesOut</b>

</td>
<td width="60%">
tcpEStatsPerfDataOctetsOut

</td>
</tr>
<tr>
<td width="40%">
<a id="DataSegsOut"></a><a id="datasegsout"></a><a id="DATASEGSOUT"></a><b>DataSegsOut</b>

</td>
<td width="60%">
tcpEStatsPerfDataSegsOut

</td>
</tr>
<tr>
<td width="40%">
<a id="DataBytesIn"></a><a id="databytesin"></a><a id="DATABYTESIN"></a><b>DataBytesIn</b>

</td>
<td width="60%">
tcpEStatsPerfDataOctetsIn

</td>
</tr>
<tr>
<td width="40%">
<a id="DataSegsIn"></a><a id="datasegsin"></a><a id="DATASEGSIN"></a><b>DataSegsIn</b>

</td>
<td width="60%">
tcpEStatsPerfDataSegsIn

</td>
</tr>
<tr>
<td width="40%">
<a id="SegsOut"></a><a id="segsout"></a><a id="SEGSOUT"></a><b>SegsOut</b>

</td>
<td width="60%">
tcpEStatsPerfSegsOut

</td>
</tr>
<tr>
<td width="40%">
<a id="SegsIn"></a><a id="segsin"></a><a id="SEGSIN"></a><b>SegsIn</b>

</td>
<td width="60%">
tcpEStatsPerfSegsIn

</td>
</tr>
<tr>
<td width="40%">
<a id="SoftErrors"></a><a id="softerrors"></a><a id="SOFTERRORS"></a><b>SoftErrors</b>

</td>
<td width="60%">
tcpEStatsStackSoftErrors

</td>
</tr>
<tr>
<td width="40%">
<a id="SoftErrorReason"></a><a id="softerrorreason"></a><a id="SOFTERRORREASON"></a><b>SoftErrorReason</b>

</td>
<td width="60%">
tcpEStatsStackSoftErrorReason

</td>
</tr>
<tr>
<td width="40%">
<a id="SndUna"></a><a id="snduna"></a><a id="SNDUNA"></a><b>SndUna</b>

</td>
<td width="60%">
tcpEStatsAppSndUna

</td>
</tr>
<tr>
<td width="40%">
<a id="SndNxt"></a><a id="sndnxt"></a><a id="SNDNXT"></a><b>SndNxt</b>

</td>
<td width="60%">
tcpEStatsAppSndNxt

</td>
</tr>
<tr>
<td width="40%">
<a id="SndMax"></a><a id="sndmax"></a><a id="SNDMAX"></a><b>SndMax</b>

</td>
<td width="60%">
tcpEStatsAppSndMax

</td>
</tr>
<tr>
<td width="40%">
<a id="ThruBytesAcked"></a><a id="thrubytesacked"></a><a id="THRUBYTESACKED"></a><b>ThruBytesAcked</b>

</td>
<td width="60%">
tcpEStatsAppThruOctetsAcked

</td>
</tr>
<tr>
<td width="40%">
<a id="RcvNxt"></a><a id="rcvnxt"></a><a id="RCVNXT"></a><b>RcvNxt</b>

</td>
<td width="60%">
tcpEStatsAppRcvNxt

</td>
</tr>
<tr>
<td width="40%">
<a id="ThruBytesReceived"></a><a id="thrubytesreceived"></a><a id="THRUBYTESRECEIVED"></a><b>ThruBytesReceived</b>

</td>
<td width="60%">
tcpEStatsAppThruOctetsReceived

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>