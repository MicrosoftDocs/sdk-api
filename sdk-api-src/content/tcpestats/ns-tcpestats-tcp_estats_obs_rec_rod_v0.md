---
UID: NS:tcpestats._TCP_ESTATS_OBS_REC_ROD_v0
title: TCP_ESTATS_OBS_REC_ROD_v0 (tcpestats.h)
description: Contains read-only dynamic information for extended TCP statistics observed on the remote receiver for a TCP connection.
helpviewer_keywords: ["*PTCP_ESTATS_OBS_REC_ROD_v0","PTCP_ESTATS_OBS_REC_ROD_v0","PTCP_ESTATS_OBS_REC_ROD_v0 structure pointer [IP Helper]","TCP_ESTATS_OBS_REC_ROD_v0","TCP_ESTATS_OBS_REC_ROD_v0 structure [IP Helper]","iphlp.tcp_estats_obs_rec_rod_v0","tcpestats/PTCP_ESTATS_OBS_REC_ROD_v0","tcpestats/TCP_ESTATS_OBS_REC_ROD_v0"]
old-location: iphlp\tcp_estats_obs_rec_rod_v0.htm
tech.root: IpHlp
ms.assetid: f790e107-0db3-4691-98fc-378518b04a8a
ms.date: 12/05/2018
ms.keywords: '*PTCP_ESTATS_OBS_REC_ROD_v0, PTCP_ESTATS_OBS_REC_ROD_v0, PTCP_ESTATS_OBS_REC_ROD_v0 structure pointer [IP Helper], TCP_ESTATS_OBS_REC_ROD_v0, TCP_ESTATS_OBS_REC_ROD_v0 structure [IP Helper], iphlp.tcp_estats_obs_rec_rod_v0, tcpestats/PTCP_ESTATS_OBS_REC_ROD_v0, tcpestats/TCP_ESTATS_OBS_REC_ROD_v0'
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
req.typenames: TCP_ESTATS_OBS_REC_ROD_v0, *PTCP_ESTATS_OBS_REC_ROD_v0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_ESTATS_OBS_REC_ROD_v0
 - tcpestats/_TCP_ESTATS_OBS_REC_ROD_v0
 - PTCP_ESTATS_OBS_REC_ROD_v0
 - tcpestats/PTCP_ESTATS_OBS_REC_ROD_v0
 - TCP_ESTATS_OBS_REC_ROD_v0
 - tcpestats/TCP_ESTATS_OBS_REC_ROD_v0
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
 - TCP_ESTATS_OBS_REC_ROD_v0
---

# TCP_ESTATS_OBS_REC_ROD_v0 structure


## -description

The <b>TCP_ESTATS_OBS_REC_ROD_v0</b> structure contains read-only dynamic information for extended TCP statistics observed on the remote receiver for a TCP connection.

## -struct-fields

### -field CurRwinRcvd

Type: <b>ULONG</b>

The most recent window advertisement, in bytes, received from the remote receiver.

### -field MaxRwinRcvd

Type: <b>ULONG</b>

The maximum window advertisement, in bytes, received from the remote receiver.

### -field MinRwinRcvd

Type: <b>ULONG</b>

The minimum window advertisement, in bytes, received from the remote receiver.

### -field WinScaleRcvd

Type: <b>ULONG</b>

The value of the received window scale option if one was
           received from the remote receiver; otherwise, a value of -1.

Note that if both the <b>WinScaleSent</b> member of the  <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_rec_rod_v0">TCP_ESTATS_REC_ROD_v0</a> structure  and
           the <b>WinScaleRcvd</b> member are not -1, then Snd.Wind.Scale
           will be the same as this value and used to scale receiver
           window announcements from the remote host to the local
           host.

## -remarks

The <b>TCP_ESTATS_OBS_REC_ROD_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_OBS_REC_ROD_v0</b> is defined as version 0 of the structure for  read-only dynamic information for extended TCP statistics on the local receiver for a TCP connection.  This information is available after the connection has been established.

The <b>TCP_ESTATS_OBS_REC_ROD_v0</b> structure is retrieved by calls to  the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsObsRec</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics need to be enabled to retrieve this structure.

The members of this structure are defined in the IETF RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://tools.ietf.org/html/rfc4898">http://www.ietf.org/rfc/rfc4898.txt</a>.




The following is the mapping of the members in the <b>TCP_ESTATS_OBS_REC_ROD_v0</b> structure to the entries defined in RFC 4898 for extended TCP statistics:



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="CurRwinRcvd"></a><a id="currwinrcvd"></a><a id="CURRWINRCVD"></a><b>CurRwinRcvd</b>

</td>
<td width="60%">
tcpEStatsPerfCurRwinRcvd

</td>
</tr>
<tr>
<td width="40%">
<a id="MaxRwinRcvd"></a><a id="maxrwinrcvd"></a><a id="MAXRWINRCVD"></a><b>MaxRwinRcvd</b>

</td>
<td width="60%">
tcpEStatsPerfMaxRwinRcvd

</td>
</tr>
<tr>
<td width="40%">
<a id="MinRwinRcvd"></a><a id="minrwinrcvd"></a><a id="MINRWINRCVD"></a><b>MinRwinRcvd</b>

</td>
<td width="60%">
No mapping to this member.

</td>
</tr>
<tr>
<td width="40%">
<a id="WinScaleRcvd"></a><a id="winscalercvd"></a><a id="WINSCALERCVD"></a><b>WinScaleRcvd</b>

</td>
<td width="60%">
tcpEStatsStackWinScaleRcvd

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>