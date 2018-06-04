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

# _TCP_ESTATS_SEND_BUFF_ROD_v0 structure


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

The <b>TCP_ESTATS_SEND_BUFF_ROD_v0</b> structure is retrieved by calls to  the <a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a> or <a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsSendBuff</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics need to be enabled to retrieve this structure.

The members of this structure are defined in the IETF RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=121686">http://www.ietf.org/rfc/rfc4898.txt</a>.




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




<a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a>
 

 

