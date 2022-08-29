---
UID: NS:tcpmib._MIB_TCPSTATS_LH
title: MIB_TCPSTATS_LH (tcpmib.h)
description: MIB_TCPSTATS_LH (tcpmib.h) contains statistics for the TCP protocol running on the local computer.
helpviewer_keywords: ["*PMIB_TCPSTATS","*PMIB_TCPSTATS_LH","MIB_TCPSTATS","MIB_TCPSTATS structure [MIB]","MIB_TCPSTATS_LH","MIB_TCPSTATS_W2K","MIB_TCP_RTO_CONSTANT","MIB_TCP_RTO_OTHER","MIB_TCP_RTO_RSRE","MIB_TCP_RTO_VANJ","PMIB_TCPSTATS","PMIB_TCPSTATS structure pointer [MIB]","_mpr_mib_tcpstats","iprtrmib/MIB_TCPSTATS","iprtrmib/PMIB_TCPSTATS","mib.mib_tcpstats","rras.mib_tcpstats","tcpmib/MIB_TCPSTATS","tcpmib/PMIB_TCPSTATS"]
old-location: mib\mib_tcpstats.htm
tech.root: MIB
ms.assetid: 08d85d02-62a0-479d-bf56-5dad452436f3
ms.date: 08/03/2022
ms.keywords: '*PMIB_TCPSTATS, *PMIB_TCPSTATS_LH, MIB_TCPSTATS, MIB_TCPSTATS structure [MIB], MIB_TCPSTATS_LH, MIB_TCPSTATS_W2K, MIB_TCP_RTO_CONSTANT, MIB_TCP_RTO_OTHER, MIB_TCP_RTO_RSRE, MIB_TCP_RTO_VANJ, PMIB_TCPSTATS, PMIB_TCPSTATS structure pointer [MIB], _mpr_mib_tcpstats, iprtrmib/MIB_TCPSTATS, iprtrmib/PMIB_TCPSTATS, mib.mib_tcpstats, rras.mib_tcpstats, tcpmib/MIB_TCPSTATS, tcpmib/PMIB_TCPSTATS'
req.header: tcpmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MIB_TCPSTATS_LH, *PMIB_TCPSTATS_LH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_TCPSTATS_LH
 - tcpmib/_MIB_TCPSTATS_LH
 - PMIB_TCPSTATS_LH
 - tcpmib/PMIB_TCPSTATS_LH
 - MIB_TCPSTATS_LH
 - tcpmib/MIB_TCPSTATS_LH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpmib.h
 - Iprtrmib.h
api_name:
 - MIB_TCPSTATS
---

# MIB_TCPSTATS_LH structure


## -description

The 
<b>MIB_TCPSTATS</b> structure contains statistics for the TCP protocol running on the local computer.

## -struct-fields

### -field dwRtoAlgorithm

Type: <b>DWORD</b>

The retransmission time-out (RTO) algorithm in use. This member can be one of the following values: 



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

### -field dwInSegs

Type: <b>DWORD</b>

The number of segments received.

### -field dwOutSegs

Type: <b>DWORD</b>

The number of segments transmitted. This number does not include retransmitted segments.

### -field dwRetransSegs

Type: <b>DWORD</b>

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

## -remarks

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatistics">GetTcpStatistics</a> function returns a pointer to a <b>MIB_TCPSTATS</b> structure. 

The <b>MIB_TCPSTATS</b> structure changed slightly on Windows Vista and later. On Windows Vista and later, the <b>dwRtoAlgorithm</b> member is replaced by  a union that contains the following members.



<table>
<tr>
<th>Member</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="DWORD_dwRtoAlgorithm"></a><a id="dword_dwrtoalgorithm"></a><a id="DWORD_DWRTOALGORITHM"></a>DWORD dwRtoAlgorithm

</td>
<td width="60%">
The retransmission time-out (RTO) algorithm in use. 

</td>
</tr>
<tr>
<td width="40%">
<a id="TCP_RTO_ALGORITHM_RtoAlgorithm"></a><a id="tcp_rto_algorithm_rtoalgorithm"></a><a id="TCP_RTO_ALGORITHM_RTOALGORITHM"></a>TCP_RTO_ALGORITHM RtoAlgorithm

</td>
<td width="60%">
The retransmission time-out (RTO) algorithm in use.  This member can be one of the values from the <b>TCP_RTO_ALGORITHM</b> enumeration type defined in the <i>Tcpmib.h</i> header file. The possible values are the same as those defined for the <b>dwRtoAlgorithm</b> member. 

</td>
</tr>
</table>
 

In the Windows SDK, the version of the structure for use on Windows Vista and later is  defined as <b>MIB_TCPSTATS_LH</b>. In the Windows SDK, the version of this structure to be used on earlier systems including Windows 2000 and later is defined as <b>MIB_TCPSTATS_W2K</b>. When compiling an application if the target platform is Windows Vista and later (<code>NTDDI_VERSION &gt;= NTDDI_LONGHORN</code>, <code>_WIN32_WINNT &gt;= 0x0600</code>, or <code>WINVER &gt;= 0x0600</code>), the <b>MIB_TCPSTATS_LH</b> structure is typedefed to the <b>MIB_TCPSTATS</b> structure. When compiling an application if the target platform is not Windows Vista and later, the <b>MIB_TCPSTATS_W2K</b> structure is typedefed to the <b>MIB_TCPSTATS</b> structure. 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Tcpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatistics">GetTcpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatistics">GetUdpStatistics</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udpstats">MIB_UDPSTATS</a>
