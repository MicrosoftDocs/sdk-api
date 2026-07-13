---
UID: NS:tcpmib._MIB_TCPSTATS2
title: MIB_TCPSTATS2 (tcpmib.h)
description: Contains statistics for the TCP protocol running on the local computer. (MIB_TCPSTATS2)
helpviewer_keywords: ["*PMIB_TCPSTATS2","MIB_TCPSTATS2","MIB_TCPSTATS2 structure [MIB]","MIB_TCP_RTO_CONSTANT","MIB_TCP_RTO_OTHER","MIB_TCP_RTO_RSRE","MIB_TCP_RTO_VANJ","PMIB_TCPSTATS2","PMIB_TCPSTATS2 structure pointer [MIB]","mib.mib_tcpstats2","tcpmib/MIB_TCPSTATS2","tcpmib/PMIB_TCPSTATS2"]
old-location: mib\mib_tcpstats2.htm
tech.root: MIB
ms.assetid: A32AA866-406B-4BE0-A4F1-5EBC9DFD646D
ms.date: 12/05/2018
ms.keywords: '*PMIB_TCPSTATS2, MIB_TCPSTATS2, MIB_TCPSTATS2 structure [MIB], MIB_TCP_RTO_CONSTANT, MIB_TCP_RTO_OTHER, MIB_TCP_RTO_RSRE, MIB_TCP_RTO_VANJ, PMIB_TCPSTATS2, PMIB_TCPSTATS2 structure pointer [MIB], mib.mib_tcpstats2, tcpmib/MIB_TCPSTATS2, tcpmib/PMIB_TCPSTATS2'
req.header: tcpmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: MIB_TCPSTATS2, *PMIB_TCPSTATS2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_TCPSTATS2
 - tcpmib/_MIB_TCPSTATS2
 - PMIB_TCPSTATS2
 - tcpmib/PMIB_TCPSTATS2
 - MIB_TCPSTATS2
 - tcpmib/MIB_TCPSTATS2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpmib.h
api_name:
 - MIB_TCPSTATS2
---

# MIB_TCPSTATS2 structure


## -description



The 
<b>MIB_TCPSTATS2</b> structure contains statistics for the TCP protocol running on the local computer. This structure is different from <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcpstats_lh">MIB_TCPSTATS</a> structure in that it uses 64-bit counters, rather than 32-bit counters.

## -struct-fields

### -field RtoAlgorithm

### -field dwRtoMin

Type: <b>DWORD</b>

The minimum RTO value in milliseconds.

### -field dwRtoMax

Type: <b>DWORD</b>

The maximum RTO value in milliseconds.

### -field dwMaxConn

Type: <b>DWORD</b>

The maximum number of connections. If this member is -1, the maximum number of connections is variable.

### -field dwActiveOpens

Type: <b>DWORD</b>

The number of active opens. In an active open, the client is initiating a connection with the server.

### -field dwPassiveOpens

Type: <b>DWORD</b>

The number of passive opens. In a passive open, the server is listening for a connection request from a client.

### -field dwAttemptFails

Type: <b>DWORD</b>

The number of failed connection attempts.

### -field dwEstabResets

Type: <b>DWORD</b>

The number of established connections that were reset.

### -field dwCurrEstab

Type: <b>DWORD</b>

The number of currently established connections.

### -field dw64InSegs

Type: <b>DWORD</b>

The number of segments received.

### -field dw64OutSegs

Type: <b>DWORD64</b>

The number of segments transmitted. This number does not include retransmitted segments.

### -field dwRetransSegs

Type: <b>DWORD64</b>

The number of segments retransmitted.

### -field dwInErrs

Type: <b>DWORD</b>

The number of errors received.

### -field dwOutRsts

Type: <b>DWORD</b>

The number of segments transmitted with the reset flag set.

### -field dwNumConns

Type: <b>DWORD</b>

The number of connections that are currently present in the system. This total number includes connections in all states except listening connections.


#### - TCP_RTO_ALGORITHM

Type: <b>DWORD</b>

The retransmission time-out (RTO) algorithm in use.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_RTO_OTHER"></a><a id="mib_tcp_rto_other"></a><dl>
<dt><b>MIB_TCP_RTO_OTHER</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Other

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_RTO_CONSTANT"></a><a id="mib_tcp_rto_constant"></a><dl>
<dt><b>MIB_TCP_RTO_CONSTANT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Constant Time-out

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_RTO_RSRE"></a><a id="mib_tcp_rto_rsre"></a><dl>
<dt><b>MIB_TCP_RTO_RSRE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
MIL-STD-1778 Appendix B

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_RTO_VANJ"></a><a id="mib_tcp_rto_vanj"></a><dl>
<dt><b>MIB_TCP_RTO_VANJ</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Van Jacobson's Algorithm

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatisticsex2">GetTcpStatisticsEx2</a> function returns a pointer to a <b>MIB_TCPSTATS2</b> structure. 

 This  structure is defined in the <i>Tcpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.
