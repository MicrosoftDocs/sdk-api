---
UID: NE:tcpestats.__unnamed_enum_0
title: TCP_ESTATS_TYPE (tcpestats.h)
author: windows-sdk-content
description: Defines the type of extended statistics for a TCP connection that is requested or being set.
old-location: iphlp\tcp_estats_type.htm
tech.root: IpHlp
ms.assetid: 96f55528-e74a-4360-a7a2-54ba19c3a284
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PTCP_ESTATS_TYPE, TCP_ESTATS_TYPE, TCP_ESTATS_TYPE enumeration [IP Helper], TcpConnectionEstatsBandwidth, TcpConnectionEstatsData, TcpConnectionEstatsFineRtt, TcpConnectionEstatsMaximum, TcpConnectionEstatsObsRec, TcpConnectionEstatsPath, TcpConnectionEstatsRec, TcpConnectionEstatsSendBuff, TcpConnectionEstatsSndCong, TcpConnectionEstatsSynOpts, iphlp.tcp_estats_type, tcpestats/TCP_ESTATS_TYPE, tcpestats/TcpConnectionEstatsBandwidth, tcpestats/TcpConnectionEstatsData, tcpestats/TcpConnectionEstatsFineRtt, tcpestats/TcpConnectionEstatsMaximum, tcpestats/TcpConnectionEstatsObsRec, tcpestats/TcpConnectionEstatsPath, tcpestats/TcpConnectionEstatsRec, tcpestats/TcpConnectionEstatsSendBuff, tcpestats/TcpConnectionEstatsSndCong, tcpestats/TcpConnectionEstatsSynOpts"
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpestats.h
api_name:
 - TCP_ESTATS_TYPE
product: Windows
targetos: Windows
req.typenames: TCP_ESTATS_TYPE, *PTCP_ESTATS_TYPE
req.redist: 
ms.custom: 19H1
---

# TCP_ESTATS_TYPE enumeration


## -description


The <b>TCP_ESTATS_TYPE</b> enumeration defines the type of extended statistics for a TCP connection that is requested or being set. 


## -enum-fields




### -field TcpConnectionEstatsSynOpts

This value specifies SYN exchange information for a TCP connection.

Only read-only static information is available for this enumeration value.


### -field TcpConnectionEstatsData

This value specifies extended data transfer information for a TCP connection.

Only read-only dynamic information and read/write information are available for this enumeration value.


### -field TcpConnectionEstatsSndCong

This value specifies sender congestion for a TCP connection.

All three types of information (read-only static, read-only dynamic,  and read/write information) are available for this enumeration value.


### -field TcpConnectionEstatsPath

This value specifies extended path measurement information for a TCP connection. This information is  used to infer segment
   reordering on the path from the local sender to the remote
   receiver.

Only read-only dynamic information and read/write information are available for this enumeration value.


### -field TcpConnectionEstatsSendBuff

This value specifies extended output-queuing information for a TCP connection.

Only read-only dynamic information and read/write information are available for this enumeration value.


### -field TcpConnectionEstatsRec

This value specifies extended local-receiver information for a TCP connection. 

Only read-only dynamic information and read/write information are available for this enumeration value.


### -field TcpConnectionEstatsObsRec

This value specifies extended remote-receiver information for a TCP connection.

Only read-only dynamic information and read/write information are available for this enumeration value.


### -field TcpConnectionEstatsBandwidth

This value specifies bandwidth estimation statistics for a TCP connection on bandwidth.

Only read-only dynamic information and read/write information are available for this enumeration value.


### -field TcpConnectionEstatsFineRtt

This value specifies fine-grained round-trip time (RTT) estimation statistics for a TCP connection.

Only read-only dynamic information and read/write information are available for this enumeration value.


### -field TcpConnectionEstatsMaximum

The maximum possible value for the <a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a>_STATE enumeration type. This is not a legal value for the possible type of extended statistics for a TCP connection.


## -remarks



The <b>TCP_ESTATS_TYPE</b> enumeration is defined on Windows Vista and later. 

The <a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a> and <b>GetPerTcp6ConnectionEStats</b> functions are designed to use TCP to diagnose performance
   problems in both the network and the application.  If a network based
   application is performing poorly, TCP can determine if the bottleneck
   is in the sender, the receiver or the network itself.  If the
   bottleneck is in the network, TCP can provide specific information
   about its nature.


The <a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a> and <b>GetPerTcp6ConnectionEStats</b> functions  are used to retrieve extended statistics for a TCP connection based on the type of extended statistics specified using one of values from the <b>TCP_ESTATS_TYPE</b> enumeration type. The collection of extended statistics on a TCP connection are enabled and disabled using calls to the <a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a> and <a href="https://msdn.microsoft.com/96d838ca-69e3-4a73-b969-3e6e810a0a69">SetPerTcpConnectionEStats</a> functions where the type of extended statistics specified is one of values from the <b>TCP_ESTATS_TYPE</b> enumeration type.




## -see-also




<a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/96d838ca-69e3-4a73-b969-3e6e810a0a69">SetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/330d06a2-9966-4e2b-b1bd-44c0f1b9416d">TCP_ESTATS_BANDWIDTH_ROD_v0</a>



<a href="https://msdn.microsoft.com/a9bf5ad3-a8db-4194-8e47-5a7409391f4c">TCP_ESTATS_BANDWIDTH_RW_v0</a>



<a href="https://msdn.microsoft.com/1e896660-10dd-471a-b4ae-116caa7a9d48">TCP_ESTATS_DATA_ROD_v0</a>



<a href="https://msdn.microsoft.com/823cea66-f719-40f6-82bd-572623188446">TCP_ESTATS_DATA_RW_v0</a>



<a href="https://msdn.microsoft.com/e33cd21f-1ec8-4715-a5e1-431a8a7e61df">TCP_ESTATS_FINE_RTT_ROD_v0</a>



<a href="https://msdn.microsoft.com/35834c9a-2896-4c11-aef7-c55af7f6fef3">TCP_ESTATS_FINE_RTT_RW_v0</a>



<a href="https://msdn.microsoft.com/f790e107-0db3-4691-98fc-378518b04a8a">TCP_ESTATS_OBS_REC_ROD_v0</a>



<a href="https://msdn.microsoft.com/91c2d5d9-3198-42a7-abf7-077281b491f2">TCP_ESTATS_OBS_REC_RW_v0</a>



<a href="https://msdn.microsoft.com/35ed2a10-caac-4004-80ac-f62c3880f5de">TCP_ESTATS_PATH_ROD_v0</a>



<a href="https://msdn.microsoft.com/460ad710-06aa-490a-9bac-5a8c731687e9">TCP_ESTATS_PATH_RW_v0</a>



<a href="https://msdn.microsoft.com/1481f108-1ea3-4952-9131-8b15e373d83e">TCP_ESTATS_REC_ROD_v0</a>



<a href="https://msdn.microsoft.com/e780ae7b-30c6-4890-8a8b-9e0b2739c176">TCP_ESTATS_REC_RW_v0</a>



<a href="https://msdn.microsoft.com/7cda7378-95e4-4f1d-88b3-27974fedec83">TCP_ESTATS_SEND_BUFF_ROD_v0</a>



<a href="https://msdn.microsoft.com/1bc88d95-24d2-4ca3-9f4a-298d5c08f4de">TCP_ESTATS_SEND_BUFF_RW_v0</a>



<a href="https://msdn.microsoft.com/5eb2d1c6-d4ba-4038-b598-ead517679ae7">TCP_ESTATS_SND_CONG_ROD_v0</a>



<a href="https://msdn.microsoft.com/4c92af92-ed51-4548-873f-b25207ea46dc">TCP_ESTATS_SND_CONG_ROS_v0</a>



<a href="https://msdn.microsoft.com/7fc7fb6a-4486-450f-b60e-8cf07b33c79a">TCP_ESTATS_SND_CONG_RW_v0</a>



<a href="https://msdn.microsoft.com/e183b23c-ce87-4818-b6d6-2305a3aa345d">TCP_ESTATS_SYN_OPTS_ROS_v0</a>
 

 

