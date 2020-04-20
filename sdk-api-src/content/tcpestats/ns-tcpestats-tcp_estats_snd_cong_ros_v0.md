---
UID: NS:tcpestats._TCP_ESTATS_SND_CONG_ROS_v0
title: TCP_ESTATS_SND_CONG_ROS_v0 (tcpestats.h)
description: Contains read-only static information for extended TCP statistics on the maximum congestion window for a TCP connection.helpviewer_keywords: ["*PTCP_ESTATS_SND_CONG_ROS_v0","PTCP_ESTATS_SND_CONG_ROS_v0","PTCP_ESTATS_SND_CONG_ROS_v0 structure pointer [IP Helper]","TCP_ESTATS_SND_CONG_ROS_v0","TCP_ESTATS_SND_CONG_ROS_v0 structure [IP Helper]","iphlp.tcp_estats_snd_cong_ros_v0","tcpestats/PTCP_ESTATS_SND_CONG_ROS_v0","tcpestats/TCP_ESTATS_SND_CONG_ROS_v0"]
old-location: iphlp\tcp_estats_snd_cong_ros_v0.htm
tech.root: IpHlp
ms.assetid: 4c92af92-ed51-4548-873f-b25207ea46dc
ms.date: 12/05/2018
ms.keywords: '*PTCP_ESTATS_SND_CONG_ROS_v0, PTCP_ESTATS_SND_CONG_ROS_v0, PTCP_ESTATS_SND_CONG_ROS_v0 structure pointer [IP Helper], TCP_ESTATS_SND_CONG_ROS_v0, TCP_ESTATS_SND_CONG_ROS_v0 structure [IP Helper], iphlp.tcp_estats_snd_cong_ros_v0, tcpestats/PTCP_ESTATS_SND_CONG_ROS_v0, tcpestats/TCP_ESTATS_SND_CONG_ROS_v0'
f1_keywords:
- tcpestats/TCP_ESTATS_SND_CONG_ROS_v0
dev_langs:
- c++
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
- TCP_ESTATS_SND_CONG_ROS_v0
targetos: Windows
req.typenames: TCP_ESTATS_SND_CONG_ROS_v0, *PTCP_ESTATS_SND_CONG_ROS_v0
req.redist: 
ms.custom: 19H1
---

# TCP_ESTATS_SND_CONG_ROS_v0 structure


## -description


The <b>TCP_ESTATS_SND_CONG_ROS_v0</b> structure contains read-only static information for extended TCP statistics on the maximum congestion window for a TCP connection.


## -struct-fields




### -field LimCwnd

The maximum size, in bytes, of the congestion window that may be
           used.


## -remarks



The <b>TCP_ESTATS_SND_CONG_ROS_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_SND_CONG_ROS_v0</b> is defined as version 0 of the structure for  read-only dynamic information on basic sender congestion data for a TCP connection.  This information is available after the connection has been established.

The <b>TCP_ESTATS_SND_CONG_ROS_v0</b> structure is retrieved by calls to  the <a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> or <a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsSndCong</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics need to be enabled to retrieve this structure.

TCP congestion control and congestion control algorithms are discussed in detail in the IETF RFC on TCP Congestion Control. For more information, see <a href="http://tools.ietf.org/html/rfc2581">http://www.ietf.org/rfc/rfc2581.txt</a>.

The members of this structure are defined in the IETF RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://tools.ietf.org/html/rfc4898">http://www.ietf.org/rfc/rfc4898.txt</a>.




The following is the mapping of the members in the <b>TCP_ESTATS_SND_CONG_ROS_v0</b> structure to the entries defined in RFC 4898 for extended TCP statistics:



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="LimCwnd"></a><a id="limcwnd"></a><a id="LIMCWND"></a><b>LimCwnd</b>

</td>
<td width="60%">
tcpEStatsTuneLimCwnd

</td>
</tr>
</table>
 






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>
 

 

