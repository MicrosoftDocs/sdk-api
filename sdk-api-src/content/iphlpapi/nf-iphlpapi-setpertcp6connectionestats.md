---
UID: NF:iphlpapi.SetPerTcp6ConnectionEStats
title: SetPerTcp6ConnectionEStats function (iphlpapi.h)
description: Sets a value in the read/write information for an IPv6 TCP connection. This function is used to enable or disable extended statistics for an IPv6 TCP connection.
helpviewer_keywords: ["SetPerTcp6ConnectionEStats","SetPerTcp6ConnectionEStats function [IP Helper]","TcpConnectionEstatsBandwidth","TcpConnectionEstatsData","TcpConnectionEstatsFineRtt","TcpConnectionEstatsObsRec","TcpConnectionEstatsPath","TcpConnectionEstatsRec","TcpConnectionEstatsSendBuff","TcpConnectionEstatsSndCong","iphlp.setpertcp6connectionestats","iphlpapi/SetPerTcp6ConnectionEStats"]
old-location: iphlp\setpertcp6connectionestats.htm
tech.root: IpHlp
ms.assetid: 89ace750-ec32-46cb-8526-233f847ba9f4
ms.date: 12/05/2018
ms.keywords: SetPerTcp6ConnectionEStats, SetPerTcp6ConnectionEStats function [IP Helper], TcpConnectionEstatsBandwidth, TcpConnectionEstatsData, TcpConnectionEstatsFineRtt, TcpConnectionEstatsObsRec, TcpConnectionEstatsPath, TcpConnectionEstatsRec, TcpConnectionEstatsSendBuff, TcpConnectionEstatsSndCong, iphlp.setpertcp6connectionestats, iphlpapi/SetPerTcp6ConnectionEStats
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
 - SetPerTcp6ConnectionEStats
 - iphlpapi/SetPerTcp6ConnectionEStats
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
 - SetPerTcp6ConnectionEStats
---

# SetPerTcp6ConnectionEStats function


## -description

The 
<b>SetPerTcp6ConnectionEStats</b> function sets a value in the read/write information for an IPv6 TCP connection. This function is used to enable or disable extended statistics for an IPv6 TCP connection.

## -parameters

### -param Row

A pointer to a <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a> structure for an IPv6 TCP connection.

### -param EstatsType

The type of extended statistics for TCP to set. This parameter determines the data and format of information that is expected in the <i>Rw</i> parameter.

This parameter can be one of the values from the <a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a> enumeration type defined in the <i>Tcpestats.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsData"></a><a id="tcpconnectionestatsdata"></a><a id="TCPCONNECTIONESTATSDATA"></a><dl>
<dt><b>TcpConnectionEstatsData</b></dt>
</dl>
</td>
<td width="60%">
This value specifies extended data transfer information for a TCP connection. 

When this value is specified, the buffer pointed to by the <i>Rw</i> parameter should point to a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_data_rw_v0">TCP_ESTATS_DATA_RW_v0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsSndCong"></a><a id="tcpconnectionestatssndcong"></a><a id="TCPCONNECTIONESTATSSNDCONG"></a><dl>
<dt><b>TcpConnectionEstatsSndCong</b></dt>
</dl>
</td>
<td width="60%">
This value specifies sender congestion for a TCP connection. 

When this value is specified, the buffer pointed to by the <i>Rw</i> parameter should point to a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_snd_cong_rw_v0">TCP_ESTATS_SND_CONG_RW_v0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsPath"></a><a id="tcpconnectionestatspath"></a><a id="TCPCONNECTIONESTATSPATH"></a><dl>
<dt><b>TcpConnectionEstatsPath</b></dt>
</dl>
</td>
<td width="60%">
This value specifies extended path measurement information for a TCP connection.

When this value is specified, the buffer pointed to by the <i>Rw</i> parameter should point to a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_path_rw_v0">TCP_ESTATS_PATH_RW_v0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsSendBuff"></a><a id="tcpconnectionestatssendbuff"></a><a id="TCPCONNECTIONESTATSSENDBUFF"></a><dl>
<dt><b>TcpConnectionEstatsSendBuff</b></dt>
</dl>
</td>
<td width="60%">
This value specifies extended output-queuing information for a TCP connection.

When this value is specified, the buffer pointed to by the <i>Rw</i> parameter should point to a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_send_buff_rw_v0">TCP_ESTATS_SEND_BUFF_RW_v0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsRec"></a><a id="tcpconnectionestatsrec"></a><a id="TCPCONNECTIONESTATSREC"></a><dl>
<dt><b>TcpConnectionEstatsRec</b></dt>
</dl>
</td>
<td width="60%">
This value specifies extended local-receiver information for a TCP connection.

When this value is specified, the buffer pointed to by the <i>Rw</i> parameter should point to a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_rec_rw_v0">TCP_ESTATS_REC_RW_v0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsObsRec"></a><a id="tcpconnectionestatsobsrec"></a><a id="TCPCONNECTIONESTATSOBSREC"></a><dl>
<dt><b>TcpConnectionEstatsObsRec</b></dt>
</dl>
</td>
<td width="60%">
This value specifies extended remote-receiver information for a TCP connection.

When this value is specified, the buffer pointed to by the <i>Rw</i> parameter should point to a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_obs_rec_rw_v0">TCP_ESTATS_OBS_REC_RW_v0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsBandwidth"></a><a id="tcpconnectionestatsbandwidth"></a><a id="TCPCONNECTIONESTATSBANDWIDTH"></a><dl>
<dt><b>TcpConnectionEstatsBandwidth</b></dt>
</dl>
</td>
<td width="60%">
This value specifies bandwidth estimation statistics for a TCP connection on bandwidth.

When this value is specified, the buffer pointed to by the <i>Rw</i> parameter should point to a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rw_v0">TCP_ESTATS_BANDWIDTH_RW_v0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TcpConnectionEstatsFineRtt"></a><a id="tcpconnectionestatsfinertt"></a><a id="TCPCONNECTIONESTATSFINERTT"></a><dl>
<dt><b>TcpConnectionEstatsFineRtt</b></dt>
</dl>
</td>
<td width="60%">
This value specifies fine-grained round-trip time (RTT) estimation statistics for a TCP connection.

When this value is specified, the buffer pointed to by the <i>Rw</i> parameter should point to a <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_fine_rtt_rw_v0">TCP_ESTATS_FINE_RTT_RW_v0</a> structure.

</td>
</tr>
</table>

### -param Rw

A pointer to a buffer that contains the read/write information to set. The buffer should contain a value from the <a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_boolean_optional">TCP_BOOLEAN_OPTIONAL</a> enumeration for each structure member that specifies how each member should be updated.

### -param RwVersion

The version of the read/write information to be set. This parameter should be set to zero for Windows Vista, Windows Server 2008, and Windows 7.

### -param RwSize

The size, in bytes, of the buffer pointed to by the <i>Rw</i> parameter.

### -param Offset

The offset, in bytes, to the member in the structure pointed to by the <i>Rw</i> parameter to be set.  This parameter is currently unused and must be set to zero.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

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
The supplied user buffer is not valid for the requested operation. This error is returned if the <i>Row</i> parameter is a <b>NULL</b> pointer and the <i>RwSize</i> parameter is nonzero.

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
The request is not supported. This error is returned if the <i>RwVersion</i> or the <i>Offset</i> parameter is not set to 0.

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

The <b>SetPerTcp6ConnectionEStats</b> function is defined on Windows Vista and later. 

The <b>SetPerTcp6ConnectionEStats</b> function is used to enable or disable extended statistics for the IPv6 TCP connection passed in the <i>Row</i> parameter. Extended statistics on a TCP connection are disabled by default. 

The <b>SetPerTcp6ConnectionEStats</b> function is used to set the value of a member in the read/write information for extended statistics for an IPv6 TCP connection. The type and format of the structure to be set is specified by the <i>EstatsType</i> parameter. The <i>Rw</i> parameter contains a pointer to the structure being passed. The member to set in this structure is specified by the <i>Offset</i> parameter. All members in the structure pointed to by <i>Rw</i> parameter must be specified. 

The only version of TCP connection statistics currently supported is version zero. So the <i>RwVersion</i> parameter passed to <b>SetPerTcp6ConnectionEStats</b> should be set to 0.

The structure pointed to by the <i>Rw</i> parameter passed this function depends on the enumeration value passed in the <i>EstatsType</i> parameter. The following table below indicates the structure type that should be passed in the <i>Rw</i> parameter for each possible <i>EstatsType</i> parameter type.  


<table>
<tr>
<th><i>EstatsType</i></th>
<th>Structure pointed to by <i>Rw</i></th>
</tr>
<tr>
<td><b>TcpConnectionEstatsData</b></td>
<td>
<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_data_rw_v0">TCP_ESTATS_DATA_RW_v0</a>
</td>
</tr>
<tr>
<td><b>TcpConnectionEstatsSndCong</b></td>
<td>
<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_snd_cong_rw_v0">TCP_ESTATS_SND_CONG_RW_v0</a>
</td>
</tr>
<tr>
<td><b>TcpConnectionEstatsPath</b></td>
<td>
<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_path_rw_v0">TCP_ESTATS_PATH_RW_v0</a>
</td>
</tr>
<tr>
<td><b>TcpConnectionEstatsSendBuff</b></td>
<td>
<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_send_buff_rw_v0">TCP_ESTATS_SEND_BUFF_RW_v0</a>
</td>
</tr>
<tr>
<td><b>TcpConnectionEstatsRec</b></td>
<td>
<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_rec_rw_v0">TCP_ESTATS_REC_RW_v0</a>
</td>
</tr>
<tr>
<td><b>TcpConnectionEstatsObsRec</b></td>
<td>
<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_obs_rec_rw_v0">TCP_ESTATS_OBS_REC_RW_v0</a>
</td>
</tr>
<tr>
<td><b>TcpConnectionEstatsBandwidth</b></td>
<td>
<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rw_v0">TCP_ESTATS_BANDWIDTH_RW_v0</a>
</td>
</tr>
<tr>
<td><b>TcpConnectionEstatsFineRtt</b></td>
<td>
<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_fine_rtt_rw_v0">TCP_ESTATS_FINE_RTT_RW_v0</a>
</td>
</tr>
</table>
 



The <i>Offset</i> parameter is currently unused. The possible structures pointed to by the <i>Rw</i> parameter all have a single member except for the <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rw_v0">TCP_ESTATS_BANDWIDTH_RW_v0</a> structure.  When the <i>EstatsType</i> parameter is set to <b>TcpConnectionEstatsBandwidth</b>, the <b>TCP_ESTATS_BANDWIDTH_RW_v0</b> structure pointed to by the <i>Rw</i> parameter must have both structure members set to the preferred values in a single call to the  <b>SetPerTcp6ConnectionEStats</b> function.

If the <i>RwSize</i> parameter is set to 0, the <b>SetPerTcp6ConnectionEStats</b> function returns NO_ERROR and makes no changes to the extended statistics status.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a> function is used to retrieve the IPv6 TCP connection table on the local computer. This function returns a <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table">MIB_TCP6TABLE</a> structure that contain an array of <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a> entries. The <i>Row</i> parameter passed to the <b>SetPerTcp6ConnectionEStats</b> function must be an entry for an existing IPv6 TCP connection.

Once extended statistics are enabled on a TCP connection for IPv6, an application calls the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> function to retrieve extended statistics on the TCP connection.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> function is designed to use TCP to diagnose performance
   problems in both the network and the application.  If a network based
   application is performing poorly, TCP can determine if the bottleneck
   is in the sender, the receiver or the network itself.  If the
   bottleneck is in the network, TCP can provide specific information
   about its nature.


For information on extended TCP statistics on an IPv4 connection, see the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcpconnectionestats">SetPerTcpConnectionEStats</a> functions.

The <b>SetPerTcp6ConnectionEStats</b> function can only be called by a user logged on as a member of the Administrators group. If <b>SetPerTcp6ConnectionEStats</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and Windows Server 2008. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table">MIB_TCP6TABLE</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcpconnectionestats">SetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_boolean_optional">TCP_BOOLEAN_OPTIONAL</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rw_v0">TCP_ESTATS_BANDWIDTH_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_data_rw_v0">TCP_ESTATS_DATA_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_fine_rtt_rw_v0">TCP_ESTATS_FINE_RTT_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_obs_rec_rw_v0">TCP_ESTATS_OBS_REC_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_path_rw_v0">TCP_ESTATS_PATH_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_rec_rw_v0">TCP_ESTATS_REC_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_send_buff_rw_v0">TCP_ESTATS_SEND_BUFF_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_snd_cong_rw_v0">TCP_ESTATS_SND_CONG_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>