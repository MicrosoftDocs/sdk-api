---
UID: NS:tcpestats._TCP_ESTATS_SND_CONG_ROD_v0
title: TCP_ESTATS_SND_CONG_ROD_v0 (tcpestats.h)
description: Contains read-only dynamic information for extended TCP statistics on sender congestion related data for a TCP connection.
helpviewer_keywords: ["*PTCP_ESTATS_SND_CONG_ROD_v0","PTCP_ESTATS_SND_CONG_ROD_v0","PTCP_ESTATS_SND_CONG_ROD_v0 structure pointer [IP Helper]","TCP_ESTATS_SND_CONG_ROD_v0","TCP_ESTATS_SND_CONG_ROD_v0 structure [IP Helper]","iphlp.tcp_estats_snd_cong_rod_v0","tcpestats/PTCP_ESTATS_SND_CONG_ROD_v0","tcpestats/TCP_ESTATS_SND_CONG_ROD_v0"]
old-location: iphlp\tcp_estats_snd_cong_rod_v0.htm
tech.root: IpHlp
ms.assetid: 5eb2d1c6-d4ba-4038-b598-ead517679ae7
ms.date: 12/05/2018
ms.keywords: '*PTCP_ESTATS_SND_CONG_ROD_v0, PTCP_ESTATS_SND_CONG_ROD_v0, PTCP_ESTATS_SND_CONG_ROD_v0 structure pointer [IP Helper], TCP_ESTATS_SND_CONG_ROD_v0, TCP_ESTATS_SND_CONG_ROD_v0 structure [IP Helper], iphlp.tcp_estats_snd_cong_rod_v0, tcpestats/PTCP_ESTATS_SND_CONG_ROD_v0, tcpestats/TCP_ESTATS_SND_CONG_ROD_v0'
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
req.typenames: TCP_ESTATS_SND_CONG_ROD_v0, *PTCP_ESTATS_SND_CONG_ROD_v0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_ESTATS_SND_CONG_ROD_v0
 - tcpestats/_TCP_ESTATS_SND_CONG_ROD_v0
 - PTCP_ESTATS_SND_CONG_ROD_v0
 - tcpestats/PTCP_ESTATS_SND_CONG_ROD_v0
 - TCP_ESTATS_SND_CONG_ROD_v0
 - tcpestats/TCP_ESTATS_SND_CONG_ROD_v0
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
 - TCP_ESTATS_SND_CONG_ROD_v0
---

# TCP_ESTATS_SND_CONG_ROD_v0 structure


## -description

The <b>TCP_ESTATS_SND_CONG_ROD_v0</b> structure contains read-only dynamic information for extended TCP statistics on sender congestion related data for a TCP connection.

## -struct-fields

### -field SndLimTransRwin

Type: <b>ULONG</b>

The number of transitions into the "Receiver Limited" state
           from either the "Congestion Limited" or "Sender Limited"
           states.  This state is entered whenever TCP transmission
           stops because the sender has filled the announced receiver
           window.

### -field SndLimTimeRwin

Type: <b>ULONG</b>

The cumulative time, in milliseconds, spent in the "Receiver Limited" state where TCP transmission
           stops because the sender has filled the announced receiver
           window.

### -field SndLimBytesRwin

Type: <b>SIZE_T</b>

The total number of bytes sent in the "Receiver Limited" state.

### -field SndLimTransCwnd

Type: <b>ULONG</b>

The number of transitions into the "Congestion Limited"
           state from either the "Receiver Limited" or "Sender
           Limited" states.  This state is entered whenever TCP
           transmission stops because the sender has reached some
           limit defined by TCP congestion control (the congestion window, for example) or other
           algorithms (retransmission timeouts) designed to control
           network traffic.

### -field SndLimTimeCwnd

Type: <b>ULONG</b>

The cumulative time, in milliseconds, spent in the "Congestion Limited"
           state.  When there is a
           retransmission timeout, it is counted in
           this member and not the cumulative time
           for some other state.

### -field SndLimBytesCwnd

Type: <b>SIZE_T</b>

The total number of bytes sent in the "Congestion Limited" state.

### -field SndLimTransSnd

Type: <b>ULONG</b>

The number of transitions into the "Sender Limited" state
           from either the "Receiver Limited" or "Congestion Limited"
           states.  This state is entered whenever TCP transmission
           stops due to some sender limit such as running out of
           application data or other resources and the Karn algorithm.
           When TCP stops sending data for any reason, which cannot be
           classified as "Receiver Limited" or "Congestion Limited", it
           is treated as "Sender Limited".

### -field SndLimTimeSnd

Type: <b>ULONG</b>

The cumulative time, in milliseconds, spent in the "Sender Limited" state.

### -field SndLimBytesSnd

Type: <b>SIZE_T</b>

The total number of bytes sent in the "Sender Limited" state.

### -field SlowStart

Type: <b>ULONG</b>

The number of times the congestion window has been
           increased by the "Slow Start" algorithm.

### -field CongAvoid

Type: <b>ULONG</b>

The number of times the congestion window has been
           increased by the "Congestion Avoidance" algorithm.

### -field OtherReductions

Type: <b>ULONG</b>

The number of congestion window reductions made as a result
           of anything other than congestion control algorithms other than "Slow Start" and "Congestion Avoidance" algorithms.

### -field CurCwnd

Type: <b>ULONG</b>

The size, in bytes, of the current congestion window.

### -field MaxSsCwnd

Type: <b>ULONG</b>

The maximum size, in bytes, of the congestion window size used during "Slow Start."

### -field MaxCaCwnd

Type: <b>ULONG</b>

The maximum size, in bytes, of the congestion window used during "Congestion
           Avoidance."

### -field CurSsthresh

Type: <b>ULONG</b>

The current size, in bytes, of the slow start threshold.

### -field MaxSsthresh

Type: <b>ULONG</b>

The maximum size, in bytes, of the slow start threshold, excluding the initial
           value.

### -field MinSsthresh

Type: <b>ULONG</b>

The minimum size, in bytes, of the slow start threshold.

## -remarks

The <b>TCP_ESTATS_SND_CONG_ROD_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_SND_CONG_ROD_v0</b> is defined as version 0 of the structure for  read-only dynamic information on sender congestion related data for a TCP connection.  This information is available after the connection has been established.

The <b>TCP_ESTATS_SND_CONG_ROD_v0</b> structure is retrieved by calls to  the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsSndCong</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics need to be enabled to retrieve this structure.

TCP congestion control and congestion control algorithms are discussed in detail in the IETF RFC on TCP Congestion Control. For more information, see <a href="http://tools.ietf.org/html/rfc2581">http://www.ietf.org/rfc/rfc2581.txt</a>.

The members of this structure are defined in the IETF RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://tools.ietf.org/html/rfc4898">http://www.ietf.org/rfc/rfc4898.txt</a>.




The following is the mapping of the members in the <b>TCP_ESTATS_SND_CONG_ROD_v0</b> structure to the entries defined in RFC 4898 for extended TCP statistics:



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="SndLimTransRwin"></a><a id="sndlimtransrwin"></a><a id="SNDLIMTRANSRWIN"></a><b>SndLimTransRwin</b>

</td>
<td width="60%">
tcpEStatsPerfSndLimTransRwin

</td>
</tr>
<tr>
<td width="40%">
<a id="SndLimTimeRwin"></a><a id="sndlimtimerwin"></a><a id="SNDLIMTIMERWIN"></a><b>SndLimTimeRwin</b>

</td>
<td width="60%">
tcpEStatsPerfSndLimTimeRwin

</td>
</tr>
<tr>
<td width="40%">
<a id="SndLimBytesRwin"></a><a id="sndlimbytesrwin"></a><a id="SNDLIMBYTESRWIN"></a><b>SndLimBytesRwin</b>

</td>
<td width="60%">
No mapping to this member.

</td>
</tr>
<tr>
<td width="40%">
<a id="SndLimTransCwnd"></a><a id="sndlimtranscwnd"></a><a id="SNDLIMTRANSCWND"></a><b>SndLimTransCwnd</b>

</td>
<td width="60%">
tcpEStatsPerfSndLimTransCwnd

</td>
</tr>
<tr>
<td width="40%">
<a id="SndLimTimeCwnd"></a><a id="sndlimtimecwnd"></a><a id="SNDLIMTIMECWND"></a><b>SndLimTimeCwnd</b>

</td>
<td width="60%">
tcpEStatsPerfSndLimTimeCwnd

</td>
</tr>
<tr>
<td width="40%">
<a id="SndLimBytesCwnd"></a><a id="sndlimbytescwnd"></a><a id="SNDLIMBYTESCWND"></a><b>SndLimBytesCwnd</b>

</td>
<td width="60%">
No mapping to this member.

</td>
</tr>
<tr>
<td width="40%">
<a id="SndLimTransSnd"></a><a id="sndlimtranssnd"></a><a id="SNDLIMTRANSSND"></a><b>SndLimTransSnd</b>

</td>
<td width="60%">
tcpEStatsPerfSndLimTransSnd

</td>
</tr>
<tr>
<td width="40%">
<a id="SndLimTimeSnd"></a><a id="sndlimtimesnd"></a><a id="SNDLIMTIMESND"></a><b>SndLimTimeSnd</b>

</td>
<td width="60%">
tcpEStatsPerfSndLimTimeSnd

</td>
</tr>
<tr>
<td width="40%">
<a id="SndLimBytesSnd"></a><a id="sndlimbytessnd"></a><a id="SNDLIMBYTESSND"></a><b>SndLimBytesSnd</b>

</td>
<td width="60%">
No mapping to this member.

</td>
</tr>
<tr>
<td width="40%">
<a id="SlowStart"></a><a id="slowstart"></a><a id="SLOWSTART"></a><b>SlowStart</b>

</td>
<td width="60%">
tcpEStatsStackSlowStart

</td>
</tr>
<tr>
<td width="40%">
<a id="CongAvoid"></a><a id="congavoid"></a><a id="CONGAVOID"></a><b>CongAvoid</b>

</td>
<td width="60%">
tcpEStatsStackCongAvoid

</td>
</tr>
<tr>
<td width="40%">
<a id="OtherReductions"></a><a id="otherreductions"></a><a id="OTHERREDUCTIONS"></a><b>OtherReductions</b>

</td>
<td width="60%">
tcpEStatsStackOtherReductions

</td>
</tr>
<tr>
<td width="40%">
<a id="CurCwnd"></a><a id="curcwnd"></a><a id="CURCWND"></a><b>CurCwnd</b>

</td>
<td width="60%">
tcpEStatsPerfCurCwnd

</td>
</tr>
<tr>
<td width="40%">
<a id="MaxSsCwnd"></a><a id="maxsscwnd"></a><a id="MAXSSCWND"></a><b>MaxSsCwnd</b>

</td>
<td width="60%">
tcpEStatsStackMaxSsCwnd

</td>
</tr>
<tr>
<td width="40%">
<a id="MaxCaCwnd"></a><a id="maxcacwnd"></a><a id="MAXCACWND"></a><b>MaxCaCwnd</b>

</td>
<td width="60%">
tcpEStatsStackMaxCaCwnd

</td>
</tr>
<tr>
<td width="40%">
<a id="CurSsthresh"></a><a id="curssthresh"></a><a id="CURSSTHRESH"></a><b>CurSsthresh</b>

</td>
<td width="60%">
tcpEStatsPerfCurSsthresh

</td>
</tr>
<tr>
<td width="40%">
<a id="MaxSsthresh"></a><a id="maxssthresh"></a><a id="MAXSSTHRESH"></a><b>MaxSsthresh</b>

</td>
<td width="60%">
tcpEStatsStackMaxSsthresh

</td>
</tr>
<tr>
<td width="40%">
<a id="MinSsthresh"></a><a id="minssthresh"></a><a id="MINSSTHRESH"></a><b>MinSsthresh</b>

</td>
<td width="60%">
tcpEStatsStackMinSsthresh

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>