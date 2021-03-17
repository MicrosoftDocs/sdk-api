---
UID: NS:tcpestats._TCP_ESTATS_SYN_OPTS_ROS_v0
title: TCP_ESTATS_SYN_OPTS_ROS_v0 (tcpestats.h)
description: Contains read-only static information for extended TCP statistics on SYN exchange for a TCP connection.
helpviewer_keywords: ["*PTCP_ESTATS_SYN_OPTS_ROS_v0","PTCP_ESTATS_SYN_OPTS_ROS_v0","PTCP_ESTATS_SYN_OPTS_ROS_v0 structure pointer [IP Helper]","TCP_ESTATS_SYN_OPTS_ROS_v0","TCP_ESTATS_SYN_OPTS_ROS_v0 structure [IP Helper]","iphlp.tcp_estats_syn_opts_ros_v0","tcpestats/PTCP_ESTATS_SYN_OPTS_ROS_v0","tcpestats/TCP_ESTATS_SYN_OPTS_ROS_v0"]
old-location: iphlp\tcp_estats_syn_opts_ros_v0.htm
tech.root: IpHlp
ms.assetid: e183b23c-ce87-4818-b6d6-2305a3aa345d
ms.date: 12/05/2018
ms.keywords: '*PTCP_ESTATS_SYN_OPTS_ROS_v0, PTCP_ESTATS_SYN_OPTS_ROS_v0, PTCP_ESTATS_SYN_OPTS_ROS_v0 structure pointer [IP Helper], TCP_ESTATS_SYN_OPTS_ROS_v0, TCP_ESTATS_SYN_OPTS_ROS_v0 structure [IP Helper], iphlp.tcp_estats_syn_opts_ros_v0, tcpestats/PTCP_ESTATS_SYN_OPTS_ROS_v0, tcpestats/TCP_ESTATS_SYN_OPTS_ROS_v0'
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
req.typenames: TCP_ESTATS_SYN_OPTS_ROS_v0, *PTCP_ESTATS_SYN_OPTS_ROS_v0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_ESTATS_SYN_OPTS_ROS_v0
 - tcpestats/_TCP_ESTATS_SYN_OPTS_ROS_v0
 - PTCP_ESTATS_SYN_OPTS_ROS_v0
 - tcpestats/PTCP_ESTATS_SYN_OPTS_ROS_v0
 - TCP_ESTATS_SYN_OPTS_ROS_v0
 - tcpestats/TCP_ESTATS_SYN_OPTS_ROS_v0
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
 - TCP_ESTATS_SYN_OPTS_ROS_v0
---

# TCP_ESTATS_SYN_OPTS_ROS_v0 structure


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

The <b>TCP_ESTATS_SYN_OPTS_ROS_v0</b> structure is retrieved by calls to  the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsSynOpts</b> is passed in the <i>EstatsType</i> parameter. Extended TCP statistics do not need to be enabled to retrieve this structure.

The MSS in the <b>MssRcvd</b> and <b>MssSent</b> members is the maximum data in a single TCP datagram. The MSS can be a very large value. 

The members of this structure are defined in the IETF RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://tools.ietf.org/html/rfc4898">http://www.ietf.org/rfc/rfc4898.txt</a>.




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

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>