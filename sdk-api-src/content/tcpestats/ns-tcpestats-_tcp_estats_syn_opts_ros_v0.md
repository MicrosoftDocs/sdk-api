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

# _TCP_ESTATS_SYN_OPTS_ROS_v0 structure


## -description


The <b>TCP_ESTATS_SYN_OPTS_ROS_v0</b> structure contains read-only static information for extended TCP statistics on SYN exchange for a TCP connection.


## -struct-fields




### -field ActiveOpen

Type: <b>BOOLEAN</b>

A value that indicates if the TCP connection was an active open. 

If the local connection traversed the SYN-SENT
           state, then this member is set to <b>TRUE</b>. Otherwise, this member is set to <b>FALSE</b>.


### -field MssRcvd

Type: <b>ULONG</b>

The value received in an Maximum Segment Size (MSS) option during the SYN exchange, or zero if no MSS option was received. 

This value is the maximum data in a single TCP datagram that the remote host  can receive.


### -field MssSent

Type: <b>ULONG</b>

The value sent in an MSS option during the SYN exchange, or zero if no MSS option was sent.


## -remarks



The <b>TCP_ESTATS_SYN_OPTS_ROS_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_SYN_OPTS_ROS_v0</b> is defined as version 0 of the structure for  read-only static information on SYN exchange for a TCP connection.  The TCP protocol does not permit the members of this structure to change after the SYN exchange. This information is available after the SYN exchange has completed.

The <b>TCP_ESTATS_SYN_OPTS_ROS_v0</b> structure is retrieved by calls to  the <a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a> or <a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsSynOpts</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics do not need to be enabled to retrieve this structure.

The MSS in the <b>MssRcvd</b> and <b>MssSent</b> members is the maximum data in a single TCP datagram. The MSS can be a very large value. 

The members of this structure are defined in the IETF RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=121686">http://www.ietf.org/rfc/rfc4898.txt</a>.




The following is the mapping of the members in the <b>TCP_ESTATS_SYN_OPTS_ROS_v0</b> structure to the entries defined in RFC 4898 for extended TCP statistics:



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="ActiveOpen"></a><a id="activeopen"></a><a id="ACTIVEOPEN"></a><b>ActiveOpen</b>

</td>
<td width="60%">
tcpEStatsStackActiveOpen

</td>
</tr>
<tr>
<td width="40%">
<a id="MssRcvd"></a><a id="mssrcvd"></a><a id="MSSRCVD"></a><b>MssRcvd</b>

</td>
<td width="60%">
tcpEStatsStackMSSRcvd

</td>
</tr>
<tr>
<td width="40%">
<a id="MssSent"></a><a id="msssent"></a><a id="MSSSENT"></a><b>MssSent</b>

</td>
<td width="60%">
tcpEStatsStackMSSSent

</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a>
 

 

