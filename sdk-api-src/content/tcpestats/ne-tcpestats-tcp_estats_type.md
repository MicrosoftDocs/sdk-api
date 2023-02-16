---
UID: NE:tcpestats.TCP_ESTATS_TYPE
title: TCP_ESTATS_TYPE (tcpestats.h)
description: Defines the type of extended statistics for a TCP connection that is requested or being set.
helpviewer_keywords: ["*PTCP_ESTATS_TYPE","TCP_ESTATS_TYPE","TCP_ESTATS_TYPE enumeration [IP Helper]","TcpConnectionEstatsBandwidth","TcpConnectionEstatsData","TcpConnectionEstatsFineRtt","TcpConnectionEstatsMaximum","TcpConnectionEstatsObsRec","TcpConnectionEstatsPath","TcpConnectionEstatsRec","TcpConnectionEstatsSendBuff","TcpConnectionEstatsSndCong","TcpConnectionEstatsSynOpts","iphlp.tcp_estats_type","tcpestats/TCP_ESTATS_TYPE","tcpestats/TcpConnectionEstatsBandwidth","tcpestats/TcpConnectionEstatsData","tcpestats/TcpConnectionEstatsFineRtt","tcpestats/TcpConnectionEstatsMaximum","tcpestats/TcpConnectionEstatsObsRec","tcpestats/TcpConnectionEstatsPath","tcpestats/TcpConnectionEstatsRec","tcpestats/TcpConnectionEstatsSendBuff","tcpestats/TcpConnectionEstatsSndCong","tcpestats/TcpConnectionEstatsSynOpts"]
old-location: iphlp\tcp_estats_type.htm
tech.root: IpHlp
ms.assetid: 96f55528-e74a-4360-a7a2-54ba19c3a284
ms.date: 12/05/2018
ms.keywords: '*PTCP_ESTATS_TYPE, TCP_ESTATS_TYPE, TCP_ESTATS_TYPE enumeration [IP Helper], TcpConnectionEstatsBandwidth, TcpConnectionEstatsData, TcpConnectionEstatsFineRtt, TcpConnectionEstatsMaximum, TcpConnectionEstatsObsRec, TcpConnectionEstatsPath, TcpConnectionEstatsRec, TcpConnectionEstatsSendBuff, TcpConnectionEstatsSndCong, TcpConnectionEstatsSynOpts, iphlp.tcp_estats_type, tcpestats/TCP_ESTATS_TYPE, tcpestats/TcpConnectionEstatsBandwidth, tcpestats/TcpConnectionEstatsData, tcpestats/TcpConnectionEstatsFineRtt, tcpestats/TcpConnectionEstatsMaximum, tcpestats/TcpConnectionEstatsObsRec, tcpestats/TcpConnectionEstatsPath, tcpestats/TcpConnectionEstatsRec, tcpestats/TcpConnectionEstatsSendBuff, tcpestats/TcpConnectionEstatsSndCong, tcpestats/TcpConnectionEstatsSynOpts'
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
req.typenames: TCP_ESTATS_TYPE, *PTCP_ESTATS_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PTCP_ESTATS_TYPE
 - tcpestats/PTCP_ESTATS_TYPE
 - TCP_ESTATS_TYPE
 - tcpestats/TCP_ESTATS_TYPE
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
 - TCP_ESTATS_TYPE
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

The maximum possible value for the <a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>_STATE enumeration type. This is not a legal value for the possible type of extended statistics for a TCP connection.

## -remarks

The <b>TCP_ESTATS_TYPE</b> enumeration is defined on Windows Vista and later. 

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> and <b>GetPerTcp6ConnectionEStats</b> functions are designed to use TCP to diagnose performance
   problems in both the network and the application.  If a network based
   application is performing poorly, TCP can determine if the bottleneck
   is in the sender, the receiver or the network itself.  If the
   bottleneck is in the network, TCP can provide specific information
   about its nature.


The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> and <b>GetPerTcp6ConnectionEStats</b> functions  are used to retrieve extended statistics for a TCP connection based on the type of extended statistics specified using one of values from the <b>TCP_ESTATS_TYPE</b> enumeration type. The collection of extended statistics on a TCP connection are enabled and disabled using calls to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcp6connectionestats">SetPerTcp6ConnectionEStats</a> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcpconnectionestats">SetPerTcpConnectionEStats</a> functions where the type of extended statistics specified is one of values from the <b>TCP_ESTATS_TYPE</b> enumeration type.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcp6connectionestats">SetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcpconnectionestats">SetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rod_v0">TCP_ESTATS_BANDWIDTH_ROD_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rw_v0">TCP_ESTATS_BANDWIDTH_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_data_rod_v0">TCP_ESTATS_DATA_ROD_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_data_rw_v0">TCP_ESTATS_DATA_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_fine_rtt_rod_v0">TCP_ESTATS_FINE_RTT_ROD_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_fine_rtt_rw_v0">TCP_ESTATS_FINE_RTT_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_obs_rec_rod_v0">TCP_ESTATS_OBS_REC_ROD_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_obs_rec_rw_v0">TCP_ESTATS_OBS_REC_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_path_rod_v0">TCP_ESTATS_PATH_ROD_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_path_rw_v0">TCP_ESTATS_PATH_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_rec_rod_v0">TCP_ESTATS_REC_ROD_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_rec_rw_v0">TCP_ESTATS_REC_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_send_buff_rod_v0">TCP_ESTATS_SEND_BUFF_ROD_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_send_buff_rw_v0">TCP_ESTATS_SEND_BUFF_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_snd_cong_rod_v0">TCP_ESTATS_SND_CONG_ROD_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_snd_cong_ros_v0">TCP_ESTATS_SND_CONG_ROS_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_snd_cong_rw_v0">TCP_ESTATS_SND_CONG_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_syn_opts_ros_v0">TCP_ESTATS_SYN_OPTS_ROS_v0</a>

