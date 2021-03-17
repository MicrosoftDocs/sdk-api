---
UID: NF:iphlpapi.GetPerTcpConnectionEStats
title: GetPerTcpConnectionEStats function (iphlpapi.h)
description: Retrieves extended statistics for an IPv4 TCP connection.
helpviewer_keywords: ["GetPerTcpConnectionEStats","GetPerTcpConnectionEStats function [IP Helper]","TcpConnectionEstatsBandwidth","TcpConnectionEstatsData","TcpConnectionEstatsFineRtt","TcpConnectionEstatsObsRec","TcpConnectionEstatsPath","TcpConnectionEstatsRec","TcpConnectionEstatsSendBuff","TcpConnectionEstatsSndCong","TcpConnectionEstatsSynOpts","iphlp.getpertcpconnectionestats","iphlpapi/GetPerTcpConnectionEStats"]
old-location: iphlp\getpertcpconnectionestats.htm
tech.root: IpHlp
ms.assetid: 71b9d795-6050-4a1a-9949-2c970801f52c
ms.date: 12/05/2018
ms.keywords: GetPerTcpConnectionEStats, GetPerTcpConnectionEStats function [IP Helper], TcpConnectionEstatsBandwidth, TcpConnectionEstatsData, TcpConnectionEstatsFineRtt, TcpConnectionEstatsObsRec, TcpConnectionEstatsPath, TcpConnectionEstatsRec, TcpConnectionEstatsSendBuff, TcpConnectionEstatsSndCong, TcpConnectionEstatsSynOpts, iphlp.getpertcpconnectionestats, iphlpapi/GetPerTcpConnectionEStats
req.header: iphlpapi.h
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetPerTcpConnectionEStats
 - iphlpapi/GetPerTcpConnectionEStats
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetPerTcpConnectionEStats
---

# GetPerTcpConnectionEStats function


## -description

The 
<b>GetPerTcpConnectionEStats</b> function retrieves extended statistics for an IPv4 TCP connection.

## -parameters

### -param Row

A pointer to a <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_lh">MIB_TCPROW</a> structure for an IPv4 TCP connection.

### -param EstatsType

The type of extended statistics for TCP requested. This parameter determines the data and format of information that is returned in the <i>Rw</i>, <i>Rod</i>, and <i>Ros</i> parameters if the call is successful.

This parameter can be one of the values from the <a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a> enumeration type defined in the <i>Tcpestats.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsSynOpts"></a><a id="tcpconnectionestatssynopts"></a><a id="TCPCONNECTIONESTATSSYNOPTS"></a><dl>
<dt><b>TcpConnectionEstatsSynOpts</b></dt>
</dl>
</td>
<td width="60%">
This value requests SYN exchange information for a TCP connection.

Only read-only static information is available for this enumeration value.

If the <i>Ros</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Ros</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_syn_opts_ros_v0">TCP_ESTATS_SYN_OPTS_ROS_v0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsData"></a><a id="tcpconnectionestatsdata"></a><a id="TCPCONNECTIONESTATSDATA"></a><dl>
<dt><b>TcpConnectionEstatsData</b></dt>
</dl>
</td>
<td width="60%">
This value requests extended data transfer information for a TCP connection. 

Only read-only dynamic information and read/write information are available for this enumeration value.

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_data_rw_v0">TCP_ESTATS_DATA_RW_v0</a> structure. 

If extended data transfer information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_data_rod_v0">TCP_ESTATS_DATA_ROD_v0</a> structure. 

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsSndCong"></a><a id="tcpconnectionestatssndcong"></a><a id="TCPCONNECTIONESTATSSNDCONG"></a><dl>
<dt><b>TcpConnectionEstatsSndCong</b></dt>
</dl>
</td>
<td width="60%">
This value requests sender congestion for a TCP connection. 

All three types of information (read-only static, read-only dynamic,  and read/write information) are available for this enumeration value.

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_snd_cong_rw_v0">TCP_ESTATS_SND_CONG_RW_v0</a> structure. 

If the <i>Ros</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Ros</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_snd_cong_ros_v0">TCP_ESTATS_SND_CONG_ROS_v0</a> structure.

If sender congestion information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_snd_cong_rod_v0">TCP_ESTATS_SND_CONG_ROD_v0</a> structure. 

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsPath"></a><a id="tcpconnectionestatspath"></a><a id="TCPCONNECTIONESTATSPATH"></a><dl>
<dt><b>TcpConnectionEstatsPath</b></dt>
</dl>
</td>
<td width="60%">
This value requests extended path measurement information for a TCP connection.

Only read-only dynamic information and read/write information are available for this enumeration value.

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_path_rw_v0">TCP_ESTATS_PATH_RW_v0</a> structure. 

If extended path measurement information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_path_rod_v0">TCP_ESTATS_PATH_ROD_v0</a> structure. 

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsSendBuff"></a><a id="tcpconnectionestatssendbuff"></a><a id="TCPCONNECTIONESTATSSENDBUFF"></a><dl>
<dt><b>TcpConnectionEstatsSendBuff</b></dt>
</dl>
</td>
<td width="60%">
This value requests extended output-queuing information for a TCP connection.

Only read-only dynamic information and read/write information are available for this enumeration value.

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_send_buff_rw_v0">TCP_ESTATS_SEND_BUFF_RW_v0</a> structure. 

If extended output-queuing information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_send_buff_rod_v0">TCP_ESTATS_SEND_BUFF_ROD_v0</a> structure. 

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsRec"></a><a id="tcpconnectionestatsrec"></a><a id="TCPCONNECTIONESTATSREC"></a><dl>
<dt><b>TcpConnectionEstatsRec</b></dt>
</dl>
</td>
<td width="60%">
This value requests extended local-receiver information for a TCP connection.

Only read-only dynamic information and read/write information are available for this enumeration value.

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_rec_rw_v0">TCP_ESTATS_REC_RW_v0</a> structure. 

If extended local-receiver information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_rec_rod_v0">TCP_ESTATS_REC_ROD_v0</a> structure. 

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsObsRec"></a><a id="tcpconnectionestatsobsrec"></a><a id="TCPCONNECTIONESTATSOBSREC"></a><dl>
<dt><b>TcpConnectionEstatsObsRec</b></dt>
</dl>
</td>
<td width="60%">
This value requests extended remote-receiver information for a TCP connection.

Only read-only dynamic information and read/write information are available for this enumeration value.

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_obs_rec_rw_v0">TCP_ESTATS_OBS_REC_RW_v0</a> structure. 

If extended remote-receiver information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_obs_rec_rod_v0">TCP_ESTATS_OBS_REC_ROD_v0</a> structure. 

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsBandwidth"></a><a id="tcpconnectionestatsbandwidth"></a><a id="TCPCONNECTIONESTATSBANDWIDTH"></a><dl>
<dt><b>TcpConnectionEstatsBandwidth</b></dt>
</dl>
</td>
<td width="60%">
This value requests bandwidth estimation statistics for a TCP connection on bandwidth.

Only read-only dynamic information and read/write information are available for this enumeration value.

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rw_v0">TCP_ESTATS_BANDWIDTH_RW_v0</a> structure. 

If bandwidth estimation statistics was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rod_v0">TCP_ESTATS_BANDWIDTH_ROD_v0</a> structure. 

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsFineRtt"></a><a id="tcpconnectionestatsfinertt"></a><a id="TCPCONNECTIONESTATSFINERTT"></a><dl>
<dt><b>TcpConnectionEstatsFineRtt</b></dt>
</dl>
</td>
<td width="60%">
This value requests fine-grained round-trip time (RTT) estimation statistics for a TCP connection.

Only read-only dynamic information and read/write information are available for this enumeration value.

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_fine_rtt_rw_v0">TCP_ESTATS_FINE_RTT_RW_v0</a> structure. 

If fine-grained RTT estimation statistics was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_fine_rtt_rod_v0">TCP_ESTATS_FINE_RTT_ROD_v0</a> structure. 

</td>
</tr>
</table>

### -param Rw [out]

A pointer to a buffer to receive the read/write information. This parameter may be a <b>NULL</b> pointer if an application does not want to retrieve read/write information for the TCP connection.

### -param RwVersion

The version of the read/write information requested. The current supported value is a version of zero.

### -param RwSize

The size, in bytes, of the buffer pointed to by <i>Rw</i> parameter.

### -param Ros [out]

A pointer to a buffer to receive read-only static information. This parameter may be a <b>NULL</b> pointer if an application does not want to retrieve read-only static information for the TCP connection.

### -param RosVersion

The version of the read-only static information requested. The current supported value is a version of zero.

### -param RosSize

The size, in bytes, of the buffer pointed to by the <i>Ros</i> parameter.

### -param Rod [out]

A pointer to a buffer to receive read-only dynamic information. This parameter may be a <b>NULL</b> pointer if an application does not want to retrieve read-only dynamic information  for the TCP connection.

### -param RodVersion

The version of the read-only dynamic information requested. The current supported value is a version of zero.

### -param RodSize

The size, in bytes, of the buffer pointed to by the <i>Rod</i> parameter.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
A buffer passed to a function is too small. This error is returned if the buffer pointed to by the <i>Rw</i>, <i>Ros</i>,  or <i>Rod</i> parameters is not large enough to receive the data.  This error also returned if one of the given buffers pointed to by the <i>Rw</i>, <i>Ros</i>,  or <i>Rod</i> parameters is <b>NULL</b>,
                but a length was specified in the associated <i>RwSize</i>, <i>RosSize</i>,  or <i>RodSize</i>.

This error value is returned on Windows Vista and Windows Server 2008.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is incorrect. This error is returned if the <i>Row</i> parameter is a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The supplied user buffer is not valid for the requested operation. This error is returned if one of the given buffers pointed to by the <i>Rw</i>, <i>Ros</i>,  or <i>Rod</i> parameters is <b>NULL</b>,
                but a length was specified in the associated <i>RwSize</i>, <i>RosSize</i>,  or <i>RodSize</i>. As a result, this error is returned if any of the following conditions are met:


<ul>
<li>The <i>Row</i> parameter is a <b>NULL</b> pointer and the <i>RwSize</i> parameter is nonzero.</li>
<li>The <i>Ros</i> parameter is a <b>NULL</b> pointer and the <i>RosSize</i> parameter is nonzero.</li>
<li>The <i>Rod</i> parameter is a <b>NULL</b> pointer and the <i>RodSize</i> parameter is nonzero.</li>
</ul>


This error value is returned on Windows 7 and Windows Server 2008 R2.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
This requested entry was not found. This error is returned if the TCP connection specified in the <i>Row</i> parameter could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if the <i>RwVersion</i>, <i>RosVersion</i>, or <i>RodVersion</i> parameter is not set to zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>GetPerTcpConnectionEStats</b> function is defined on Windows Vista and later. 

The <b>GetPerTcpConnectionEStats</b> function is designed to use TCP to diagnose performance
   problems in both the network and the application.  If a network based
   application is performing poorly, TCP can determine if the bottleneck
   is in the sender, the receiver or the network itself.  If the
   bottleneck is in the network, TCP can provide specific information
   about its nature.


The <b>GetPerTcpConnectionEStats</b> function retrieves extended statistics for the IPv4 TCP connection passed in the <i>Row</i> parameter. The type of extended statistics that is retrieved is specified in the <i>EstatsType</i> parameter. Extended statistics on this TCP connection must have previously been enabled by calls to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcpconnectionestats">SetPerTcpConnectionEStats</a> function for all <a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a> values except when <b>TcpConnectionEstatsSynOpts</b> is passed in the <i>EstatsType</i> parameter.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcptable">GetTcpTable</a> function is used to retrieve the IPv4 TCP connection table on the local computer. This function returns a <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a> structure that contain an array of <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_lh">MIB_TCPROW</a> entries. The <i>Row</i> parameter passed to the <b>GetPerTcpConnectionEStats</b> function must be an entry for an existing IPv4 TCP connection.

The only version of TCP connection statistics currently supported is version zero. So the <i>RwVersion</i>, <i>RosVersion</i>, and <i>RodVersion</i> parameters passed to <b>GetPerTcpConnectionEStats</b> should be set to 0.

For information on extended TCP statistics on an IPv6 connection, see the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcp6connectionestats">SetPerTcp6ConnectionEStats</a> functions.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcpconnectionestats">SetPerTcpConnectionEStats</a> function can only be called by a user logged on as a member of the Administrators group. If <b>SetPerTcpConnectionEStats</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

The caller of **GetPerTcpConnectionEStats** should check the *EnableCollection* field in the returned *Rw* struct, and if it is not `TRUE`, then the caller should ignore the data in the *Ros* and *Rod* structs. If *EnableCollection* is set to `FALSE`, then the data returned in *Ros* and *Rod* are undefined. For example, one condition under which this can happen is when you're using **GetPerTcpConnectionEStats** to retrieve extended statistics for an IPv4 TCP connection, and you've previously called [SetPerTcpConnectionEStats](./nf-iphlpapi-setpertcpconnectionestats.md) to enable extended statistics. If the **SetPerTcpConnectionEStats** call fails then subsequent calls to **GetPerTcpConnectionEStats** will return meaningless random data, and not extended TCP statistics. You can observe that example by running the example below as both an administrator, and as a normal user.

## Examples

For a code example, see the **Examples** section in the [GetPerTcp6ConnectionEStats function](./nf-iphlpapi-getpertcp6connectionestats.md) topic.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcptable">GetTcpTable</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_lh">MIB_TCPROW</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a>



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



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_soft_error">TCP_SOFT_ERROR</a>