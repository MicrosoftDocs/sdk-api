---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _MIB_TCPSTATS_W2K structure


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



The <a href="_iphlp_gettcpstatistics">GetTcpStatistics</a> function returns a pointer to a <b>MIB_TCPSTATS</b> structure. 

The <b>MIB_TCPSTATS</b> structure changed slightly on Windows Vista and later. On Windows Vista
   and later, the <b>dwRtoAlgorithm</b> member is replaced by  a union that contains the following members.



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

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista
   and later, the organization of header files has changed. This  structure is defined in the <i>Tcpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="_iphlp_gettcpstatistics">GetTcpStatistics</a>



<a href="https://msdn.microsoft.com/a86e5758-a984-4483-8e9c-c482a7676a20">GetUdpStatistics</a>



<a href="https://msdn.microsoft.com/128bae44-59a2-4e37-a588-a18805b9e340">MIB_UDPSTATS</a>
 

 

