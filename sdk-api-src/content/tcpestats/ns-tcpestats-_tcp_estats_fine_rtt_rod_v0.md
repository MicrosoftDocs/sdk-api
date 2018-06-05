---
UID: NS:tcpestats._TCP_ESTATS_FINE_RTT_ROD_v0
title: "_TCP_ESTATS_FINE_RTT_ROD_v0"
author: windows-sdk-content
description: Contains read-only dynamic information for extended TCP statistics on fine-grained round-trip time (RTT) estimation for a TCP connection.
old-location: iphlp\tcp_estats_fine_rtt_rod_v0.htm
old-project: IpHlp
ms.assetid: e33cd21f-1ec8-4715-a5e1-431a8a7e61df
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PTCP_ESTATS_FINE_RTT_ROD_v0, PTCP_ESTATS_FINE_RTT_ROD_v0, PTCP_ESTATS_FINE_RTT_ROD_v0 structure pointer [IP Helper], TCP_ESTATS_FINE_RTT_ROD_v0, TCP_ESTATS_FINE_RTT_ROD_v0 structure [IP Helper], _TCP_ESTATS_FINE_RTT_ROD_v0, iphlp.tcp_estats_fine_rtt_rod_v0, tcpestats/PTCP_ESTATS_FINE_RTT_ROD_v0, tcpestats/TCP_ESTATS_FINE_RTT_ROD_v0"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: TCP_ESTATS_FINE_RTT_ROD_v0, *PTCP_ESTATS_FINE_RTT_ROD_v0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tcpestats.h
api_name:
-	TCP_ESTATS_FINE_RTT_ROD_v0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _TCP_ESTATS_FINE_RTT_ROD_v0 structure


## -description


The <b>TCP_ESTATS_FINE_RTT_ROD_v0</b> structure contains read-only dynamic information for extended TCP statistics on fine-grained round-trip time (RTT) estimation  for a TCP connection.


## -struct-fields




### -field RttVar

Type: <b>ULONG</b>

The round trip time variation, in microseconds, used in receive window auto-tuning when the TCP extended statistics feature is enabled.


### -field MaxRtt

Type: <b>ULONG</b>

The maximum sampled round trip time, in microseconds.


### -field MinRtt

Type: <b>ULONG</b>

The minimum sampled round trip time, in microseconds.


### -field SumRtt

Type: <b>ULONG</b>

A smoothed value round trip time, in microseconds,  computed from all sampled round trip times. The smoothing is a weighted additive function that uses the <b>RttVar</b> member.


## -remarks



The <b>TCP_ESTATS_FINE_RTT_ROD_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_FINE_RTT_ROD_v0</b> is defined as version 0 of the structure for  read-only dynamic information for extended TCP statistics on fine-grained round-trip time estimation for a TCP connection.  This information is available after the connection has been established.

The <b>TCP_ESTATS_FINE_RTT_ROD_v0</b> structure is retrieved by calls to  the <a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a> or <a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsFineRtt</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics need to be enabled to retrieve this structure.

The TCP retransmission timer is discussed in detail in the IETF RFC 2988 on Computing TCP's Retransmission Timer For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=167112">http://www.ietf.org/rfc/rfc2988.txt</a>.

The members of this structure are not defined in the IETF RFC on the TCP Extended Statistics MIB. However, there are members in the <a href="https://msdn.microsoft.com/35ed2a10-caac-4004-80ac-f62c3880f5de">TCP_ESTATS_PATH_ROD_v0</a> structure that provide similar time measurements in milliseconds. For more information, see the <b>TCP_ESTATS_PATH_ROD_v0</b> structure and <a href="http://go.microsoft.com/fwlink/p/?linkid=121686">http://www.ietf.org/rfc/rfc4898.txt</a>.





## -see-also




<a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/35ed2a10-caac-4004-80ac-f62c3880f5de">TCP_ESTATS_PATH_ROD_v0</a>



<a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a>
 

 

