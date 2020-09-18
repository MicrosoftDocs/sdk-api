---
UID: NF:iphlpapi.GetPerTcp6ConnectionEStats
title: GetPerTcp6ConnectionEStats function (iphlpapi.h)
description: Retrieves extended statistics for an IPv6 TCP connection.
helpviewer_keywords: ["GetPerTcp6ConnectionEStats","GetPerTcp6ConnectionEStats function [IP Helper]","TcpConnectionEstatsBandwidth","TcpConnectionEstatsData","TcpConnectionEstatsFineRtt","TcpConnectionEstatsObsRec","TcpConnectionEstatsPath","TcpConnectionEstatsRec","TcpConnectionEstatsSendBuff","TcpConnectionEstatsSndCong","TcpConnectionEstatsSynOpts","iphlp.getpertcp6connectionestats","iphlpapi/GetPerTcp6ConnectionEStats"]
old-location: iphlp\getpertcp6connectionestats.htm
tech.root: IpHlp
ms.assetid: 291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e
ms.date: 12/05/2018
ms.keywords: GetPerTcp6ConnectionEStats, GetPerTcp6ConnectionEStats function [IP Helper], TcpConnectionEstatsBandwidth, TcpConnectionEstatsData, TcpConnectionEstatsFineRtt, TcpConnectionEstatsObsRec, TcpConnectionEstatsPath, TcpConnectionEstatsRec, TcpConnectionEstatsSendBuff, TcpConnectionEstatsSndCong, TcpConnectionEstatsSynOpts, iphlp.getpertcp6connectionestats, iphlpapi/GetPerTcp6ConnectionEStats
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
 - GetPerTcp6ConnectionEStats
 - iphlpapi/GetPerTcp6ConnectionEStats
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
 - GetPerTcp6ConnectionEStats
---

# GetPerTcp6ConnectionEStats function


## -description

The 
<b>GetPerTcp6ConnectionEStats</b> function retrieves extended statistics for an IPv6 TCP connection.

## -parameters

### -param Row

A pointer to a <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a> structure for an IPv6 TCP connection.

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

The version of the read-only dynamic information requested. The current supported value is a version of zero..

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

The <b>GetPerTcp6ConnectionEStats</b> function is defined on Windows Vista and later. 

The <b>GetPerTcp6ConnectionEStats</b> function is designed to use TCP to diagnose performance
   problems in both the network and the application.  If a network based
   application is performing poorly, TCP can determine if the bottleneck
   is in the sender, the receiver or the network itself.  If the
   bottleneck is in the network, TCP can provide specific information
   about its nature.


The <b>GetPerTcp6ConnectionEStats</b> function retrieves extended statistics for the IPv6 TCP connection passed in the <i>Row</i> parameter. The type of extended statistics that is retrieved is specified in the <i>EstatsType</i> parameter. Extended statistics on this TCP connection must have previously been enabled by calls to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcp6connectionestats">SetPerTcp6ConnectionEStats</a> function for all <a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a> values except when <b>TcpConnectionEstatsSynOpts</b> is passed in the <i>EstatsType</i> parameter. 

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a> function is used to retrieve the IPv6 TCP connection table on the local computer. This function returns a <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table">MIB_TCP6TABLE</a> structure that contain an array of <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a> entries. The <i>Row</i> parameter passed to the <b>GetPerTcp6ConnectionEStats</b> function must be an entry for an existing IPv6 TCP connection.

The only version of TCP connection statistics currently supported is version zero. So the <i>RwVersion</i>, <i>RosVersion</i>, and <i>RodVersion</i> parameters passed to <b>GetPerTcp6ConnectionEStats</b> should be set to 0.

For information on extended TCP statistics on an IPv4 connection, see the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcpconnectionestats">SetPerTcpConnectionEStats</a> functions.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcp6connectionestats">SetPerTcp6ConnectionEStats</a> function can only be called by a user logged on as a member of the Administrators group. If <b>SetPerTcp6ConnectionEStats</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

The caller of **GetPerTcp6ConnectionEStats** should check the *EnableCollection* field in the returned *Rw* struct, and if it is not `TRUE`, then the caller should ignore the data in the *Ros* and *Rod* structs. If *EnableCollection* is set to `FALSE`, then the data returned in *Ros* and *Rod* are undefined. For example, one condition under which this can happen is when you're using **GetPerTcp6ConnectionEStats** to retrieve extended statistics for an IPv6 TCP connection, and you've previously called [SetPerTcp6ConnectionEStats](./nf-iphlpapi-setpertcp6connectionestats.md) to enable extended statistics. If the **SetPerTcp6ConnectionEStats** call fails then subsequent calls to **GetPerTcp6ConnectionEStats** will return meaningless random data, and not extended TCP statistics. You can observe that example by running the example below as both an administrator, and as a normal user.

## Examples

The following example retrieves the TCP extended statistics for an IPv4 and IPv6 TCP connection and prints values from the returned data.

```cpp
// Need to link with Iphlpapi.lib and Ws2_32.lib
// Need to run as administrator

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <Ws2tcpip.h>
#include <iphlpapi.h>
#include <Tcpestats.h>
#include <stdlib.h>
#include <stdio.h>

// Need to link with Iphlpapi.lib
#pragma comment(lib, "iphlpapi.lib")

// Need to link with Ws2_32.lib
#pragma comment(lib, "ws2_32.lib")

// An array of name for the TCP_ESTATS_TYPE enum values
// The names values must match the enum values
const wchar_t* estatsTypeNames[] = {
    L"TcpConnectionEstatsSynOpts",
    L"TcpConnectionEstatsData",
    L"TcpConnectionEstatsSndCong",
    L"TcpConnectionEstatsPath",
    L"TcpConnectionEstatsSendBuff",
    L"TcpConnectionEstatsRec",
    L"TcpConnectionEstatsObsRec",
    L"TcpConnectionEstatsBandwidth",
    L"TcpConnectionEstatsFineRtt",
    L"TcpConnectionEstatsMaximum"
};

// Function prototypes

// Run tests for IPv4 or IPv4 TCP extended stats
DWORD RunEstatsTest(bool v6);

// Get an IPv4 TCP row entry
DWORD GetTcpRow(u_short localPort, u_short remotePort,
    MIB_TCP_STATE state, __out PMIB_TCPROW row);

// Get an IPv6 TCP row entry
DWORD GetTcp6Row(u_short localPort, u_short remotePort,
    MIB_TCP_STATE state, __out PMIB_TCP6ROW row);

// Enable or disable the supplied Estat type on a TCP connection
void ToggleEstat(PVOID row, TCP_ESTATS_TYPE type, bool enable, bool v6);

// Toggle all Estats for a TCP connection
void ToggleAllEstats(void* row, bool enable, bool v6);

// Dump the supplied Estate type data on the given TCP connection row
void GetAndOutputEstats(void* row, TCP_ESTATS_TYPE type, bool v6);

//
void GetAllEstats(void* row, bool v6);

// Creates a TCP server and client socket on the loopback address.
// Binds the server socket to a port.
// Establishes a client TCP connection to the server 
int CreateTcpConnection(bool v6, SOCKET* serviceSocket, SOCKET* clientSocket,
    SOCKET* acceptSocket, u_short* serverPort,
    u_short* clientPort);

//
// Entry point.
//
int __cdecl main()
{
    RunEstatsTest(FALSE);
    RunEstatsTest(TRUE);
    return (0);
}

//
// Create connect and listen sockets on loopback interface and dump all Estats
// types on the created TCP connections for the supplied IP address type.
//
DWORD RunEstatsTest(bool v6)
{
    SOCKET serviceSocket, clientSocket, acceptSocket;
    serviceSocket = clientSocket = acceptSocket = INVALID_SOCKET;
    MIB_TCPROW server4ConnectRow, client4ConnectRow;
    MIB_TCP6ROW server6ConnectRow, client6ConnectRow;
    void* serverConnectRow, * clientConnectRow = NULL;
    bool bWSAStartup = false;

    char* buff = (char*)malloc(1000);
    if (buff == NULL) {
        wprintf(L"\nFailed to allocate memory.");
        goto bail;
    }

    if (v6) {
        serverConnectRow = &server6ConnectRow;
        clientConnectRow = &client6ConnectRow;
    }
    else {
        serverConnectRow = &server4ConnectRow;
        clientConnectRow = &client4ConnectRow;
    }

    UINT winStatus;
    int sockStatus;
    u_short serverPort, clientPort;

    //
    // Initialize Winsock.
    //
    WSADATA wsaData;
    winStatus = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (winStatus != ERROR_SUCCESS) {
        wprintf(L"\nFailed to open winsock. Error %d", winStatus);
        goto bail;
    }

    bWSAStartup = true;

    //
    // Create TCP connection on which Estats information will be collected.
    // Obtain port numbers of created connections.
    //
    winStatus =
        CreateTcpConnection(v6, &serviceSocket, &clientSocket, &acceptSocket,
            &serverPort, &clientPort);
    if (winStatus != ERROR_SUCCESS) {
        wprintf(L"\nFailed to create TCP connection. Error %d", winStatus);
        goto bail;
    }
    //
    // Obtain MIB_TCPROW corresponding to the TCP connection.
    //
    winStatus = v6 ?
        GetTcp6Row(serverPort, clientPort, MIB_TCP_STATE_ESTAB,
            (PMIB_TCP6ROW)serverConnectRow) :
        GetTcpRow(serverPort, clientPort, MIB_TCP_STATE_ESTAB,
            (PMIB_TCPROW)serverConnectRow);
    if (winStatus != ERROR_SUCCESS) {
        wprintf
        (L"\nGetTcpRow failed on the server established connection with %d",
            winStatus);
        goto bail;
    }

    winStatus = v6 ?
        GetTcp6Row(clientPort, serverPort, MIB_TCP_STATE_ESTAB,
            (PMIB_TCP6ROW)clientConnectRow) :
        GetTcpRow(clientPort, serverPort, MIB_TCP_STATE_ESTAB,
            (PMIB_TCPROW)clientConnectRow);
    if (winStatus != ERROR_SUCCESS) {
        wprintf
        (L"\nGetTcpRow failed on the client established connection with %d",
            winStatus);
        goto bail;
    }
    //
    // Enable Estats collection and dump current stats.
    //
    ToggleAllEstats(serverConnectRow, TRUE, v6);
    ToggleAllEstats(clientConnectRow, TRUE, v6);
    wprintf(L"\n\n\nDumping Estats for server socket:\n");
    GetAllEstats(serverConnectRow, v6);
    wprintf(L"\n\n\nDumping Estats for client connect socket:\n");
    GetAllEstats(clientConnectRow, v6);

    //
    // Initiate TCP data transfers to see effect on Estats counters.
    //
    sockStatus = send(clientSocket, buff, (int)(1000 * sizeof(char)), 0);
    if (sockStatus == SOCKET_ERROR) {
        wprintf(L"\nFailed to send from client to server %d",
            WSAGetLastError());
    }
    else {
        sockStatus = recv(acceptSocket, buff, (int)(1000 * sizeof(char)), 0);
        if (sockStatus == SOCKET_ERROR) {
            wprintf(L"\nFailed to receive data on the server %d",
                WSAGetLastError());
        }
    }

    //
    // Dump updated Estats and disable Estats collection.
    //
    wprintf
    (L"\n\n\nDumping Estats for server socket after client sends data:\n");
    GetAllEstats(serverConnectRow, v6);
    wprintf
    (L"\n\n\nDumping Estats for client socket after client sends data:\n");
    GetAllEstats(clientConnectRow, v6);
    ToggleAllEstats(serverConnectRow, FALSE, v6);
    ToggleAllEstats(clientConnectRow, FALSE, v6);

bail:
    if (serviceSocket != INVALID_SOCKET)
        closesocket(serviceSocket);
    if (clientSocket != INVALID_SOCKET)
        closesocket(clientSocket);
    if (acceptSocket != INVALID_SOCKET)
        closesocket(acceptSocket);
    if (buff != NULL)
        free(buff);
    if (bWSAStartup)
        WSACleanup();
    return ERROR_SUCCESS;
}

int CreateTcpConnection(bool v6,
    SOCKET* serviceSocket,
    SOCKET* clientSocket,
    SOCKET* acceptSocket,
    u_short* serverPort, u_short* clientPort)
{
    INT status;
    ADDRINFOW hints, * localhost = NULL;
    const wchar_t* loopback;
    loopback = v6 ? L"::1" : L"127.0.0.1";
    int aiFamily = v6 ? AF_INET6 : AF_INET;
    int nameLen = sizeof(SOCKADDR_STORAGE);

    *serviceSocket = INVALID_SOCKET;
    *clientSocket = INVALID_SOCKET;
    *acceptSocket = INVALID_SOCKET;

    ZeroMemory(&hints, sizeof(hints));
    hints.ai_family = aiFamily;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;

    status = GetAddrInfoW(loopback, L"", &hints, &localhost);
    if (status != ERROR_SUCCESS) {
        wprintf(L"\nFailed to open localhost. Error %d", status);
        goto bail;
    }

    *serviceSocket = socket(aiFamily, SOCK_STREAM, IPPROTO_TCP);
    if (*serviceSocket == INVALID_SOCKET) {
        wprintf(L"\nFailed to create server socket. Error %d",
            WSAGetLastError());
        goto bail;
    }

    *clientSocket = socket(aiFamily, SOCK_STREAM, IPPROTO_TCP);
    if (*clientSocket == INVALID_SOCKET) {
        wprintf(L"\nFailed to create client socket. Error %d",
            WSAGetLastError());
        goto bail;
    }

    status =
        bind(*serviceSocket, localhost->ai_addr, (int)localhost->ai_addrlen);
    if (status == SOCKET_ERROR) {
        wprintf(L"\nFailed to bind server socket to loopback. Error %d",
            WSAGetLastError());
        goto bail;
    }

    if (localhost != NULL) {
        FreeAddrInfoW(localhost);
        localhost = NULL;
    }

    SOCKADDR_STORAGE serverSockName, clientSockName;
    status = getsockname(*serviceSocket,
        (sockaddr*)&serverSockName, &nameLen);
    if (status == SOCKET_ERROR) {
        wprintf(L"\ngetsockname failed %d", WSAGetLastError());
        goto bail;
    }
    if (v6) {
        *serverPort = ((sockaddr_in6*)(&serverSockName))->sin6_port;
    }
    else {
        *serverPort = ((sockaddr_in*)(&serverSockName))->sin_port;
    }

    status = listen(*serviceSocket, SOMAXCONN);
    if (status == SOCKET_ERROR) {
        wprintf(L"\nFailed to listen on server socket. Error %d",
            WSAGetLastError());
        goto bail;
    }

    status =
        connect(*clientSocket, (sockaddr*)&serverSockName,
            (int)sizeof(SOCKADDR_STORAGE));
    if (status == SOCKET_ERROR) {
        wprintf(L"\nCould not connect client and server sockets %d",
            WSAGetLastError());
        goto bail;
    }

    status = getsockname(*clientSocket,
        (sockaddr*)&clientSockName, &nameLen);
    if (status == SOCKET_ERROR) {
        wprintf(L"\ngetsockname failed %d", WSAGetLastError());
        goto bail;
    }
    if (v6) {
        *clientPort = ((sockaddr_in6*)(&clientSockName))->sin6_port;
    }
    else {
        *clientPort = ((sockaddr_in*)(&clientSockName))->sin_port;
    }

    *acceptSocket = accept(*serviceSocket, NULL, NULL);
    if (*acceptSocket == INVALID_SOCKET) {
        wprintf(L"\nFailed to accept socket connection %d", WSAGetLastError());
        goto bail;
    }

    return ERROR_SUCCESS;

bail:
    if (localhost != NULL)
        FreeAddrInfoW(localhost);

    if (*serviceSocket != INVALID_SOCKET) {
        closesocket(*serviceSocket);
        *serviceSocket = INVALID_SOCKET;
    }

    if (*clientSocket != INVALID_SOCKET) {
        closesocket(*clientSocket);
        *clientSocket = INVALID_SOCKET;
    }

    if (*acceptSocket != INVALID_SOCKET) {
        closesocket(*acceptSocket);
        *acceptSocket = INVALID_SOCKET;
    }

    return status;
}

void GetAllEstats(void* row, bool v6)
{
    GetAndOutputEstats(row, TcpConnectionEstatsSynOpts, v6);
    GetAndOutputEstats(row, TcpConnectionEstatsData, v6);
    GetAndOutputEstats(row, TcpConnectionEstatsSndCong, v6);
    GetAndOutputEstats(row, TcpConnectionEstatsPath, v6);
    GetAndOutputEstats(row, TcpConnectionEstatsSendBuff, v6);
    GetAndOutputEstats(row, TcpConnectionEstatsRec, v6);
    GetAndOutputEstats(row, TcpConnectionEstatsObsRec, v6);
    GetAndOutputEstats(row, TcpConnectionEstatsBandwidth, v6);
    GetAndOutputEstats(row, TcpConnectionEstatsFineRtt, v6);
}

//
// Returns a MIB_TCPROW corresponding to the local port, remote port and state
// filter parameters.
//
DWORD
GetTcpRow(u_short localPort,
    u_short remotePort, MIB_TCP_STATE state, __out PMIB_TCPROW row)
{
    PMIB_TCPTABLE tcpTable = NULL;
    PMIB_TCPROW tcpRowIt = NULL;

    DWORD status, size = 0, i;
    bool connectionFound = FALSE;

    status = GetTcpTable(tcpTable, &size, TRUE);
    if (status != ERROR_INSUFFICIENT_BUFFER) {
        return status;
    }

    tcpTable = (PMIB_TCPTABLE)malloc(size);
    if (tcpTable == NULL) {
        return ERROR_OUTOFMEMORY;
    }

    status = GetTcpTable(tcpTable, &size, TRUE);
    if (status != ERROR_SUCCESS) {
        free(tcpTable);
        return status;
    }

    for (i = 0; i < tcpTable->dwNumEntries; i++) {
        tcpRowIt = &tcpTable->table[i];
        if (tcpRowIt->dwLocalPort == (DWORD)localPort &&
            tcpRowIt->dwRemotePort == (DWORD)remotePort &&
            tcpRowIt->State == state) {
            connectionFound = TRUE;
            *row = *tcpRowIt;
            break;
        }
    }

    free(tcpTable);

    if (connectionFound) {
        return ERROR_SUCCESS;
    }
    else {
        return ERROR_NOT_FOUND;
    }
}

//
// Returns a MIB_TCP6ROW corresponding to the local port, remote port and state
// filter parameters. This is a v6 equivalent of the GetTcpRow function.
//
DWORD
GetTcp6Row(u_short localPort,
    u_short remotePort, MIB_TCP_STATE state, __out PMIB_TCP6ROW row)
{
    PMIB_TCP6TABLE tcp6Table = NULL;
    PMIB_TCP6ROW tcp6RowIt = NULL;

    DWORD status, size = 0, i;
    bool connectionFound = FALSE;

    status = GetTcp6Table(tcp6Table, &size, TRUE);
    if (status != ERROR_INSUFFICIENT_BUFFER) {
        return status;
    }

    tcp6Table = (PMIB_TCP6TABLE)malloc(size);
    if (tcp6Table == NULL) {
        return ERROR_OUTOFMEMORY;
    }

    status = GetTcp6Table(tcp6Table, &size, TRUE);
    if (status != ERROR_SUCCESS) {
        free(tcp6Table);
        return status;
    }

    for (i = 0; i < tcp6Table->dwNumEntries; i++) {
        tcp6RowIt = &tcp6Table->table[i];
        if (tcp6RowIt->dwLocalPort == (DWORD)localPort &&
            tcp6RowIt->dwRemotePort == (DWORD)remotePort &&
            tcp6RowIt->State == state) {
            connectionFound = TRUE;
            *row = *tcp6RowIt;
            break;
        }
    }

    free(tcp6Table);

    if (connectionFound) {
        return ERROR_SUCCESS;
    }
    else {
        return ERROR_NOT_FOUND;
    }
}

//
// Enable or disable the supplied Estat type on a TCP connection.
//
void ToggleEstat(PVOID row, TCP_ESTATS_TYPE type, bool enable, bool v6)
{
    TCP_BOOLEAN_OPTIONAL operation =
        enable ? TcpBoolOptEnabled : TcpBoolOptDisabled;
    ULONG status, size = 0;
    PUCHAR rw = NULL;
    TCP_ESTATS_DATA_RW_v0 dataRw;
    TCP_ESTATS_SND_CONG_RW_v0 sndRw;
    TCP_ESTATS_PATH_RW_v0 pathRw;
    TCP_ESTATS_SEND_BUFF_RW_v0 sendBuffRw;
    TCP_ESTATS_REC_RW_v0 recRw;
    TCP_ESTATS_OBS_REC_RW_v0 obsRecRw;
    TCP_ESTATS_BANDWIDTH_RW_v0 bandwidthRw;
    TCP_ESTATS_FINE_RTT_RW_v0 fineRttRw;

    switch (type) {
    case TcpConnectionEstatsData:
        dataRw.EnableCollection = enable;
        rw = (PUCHAR)&dataRw;
        size = sizeof(TCP_ESTATS_DATA_RW_v0);
        break;

    case TcpConnectionEstatsSndCong:
        sndRw.EnableCollection = enable;
        rw = (PUCHAR)&sndRw;
        size = sizeof(TCP_ESTATS_SND_CONG_RW_v0);
        break;

    case TcpConnectionEstatsPath:
        pathRw.EnableCollection = enable;
        rw = (PUCHAR)&pathRw;
        size = sizeof(TCP_ESTATS_PATH_RW_v0);
        break;

    case TcpConnectionEstatsSendBuff:
        sendBuffRw.EnableCollection = enable;
        rw = (PUCHAR)&sendBuffRw;
        size = sizeof(TCP_ESTATS_SEND_BUFF_RW_v0);
        break;

    case TcpConnectionEstatsRec:
        recRw.EnableCollection = enable;
        rw = (PUCHAR)&recRw;
        size = sizeof(TCP_ESTATS_REC_RW_v0);
        break;

    case TcpConnectionEstatsObsRec:
        obsRecRw.EnableCollection = enable;
        rw = (PUCHAR)&obsRecRw;
        size = sizeof(TCP_ESTATS_OBS_REC_RW_v0);
        break;

    case TcpConnectionEstatsBandwidth:
        bandwidthRw.EnableCollectionInbound = operation;
        bandwidthRw.EnableCollectionOutbound = operation;
        rw = (PUCHAR)&bandwidthRw;
        size = sizeof(TCP_ESTATS_BANDWIDTH_RW_v0);
        break;

    case TcpConnectionEstatsFineRtt:
        fineRttRw.EnableCollection = enable;
        rw = (PUCHAR)&fineRttRw;
        size = sizeof(TCP_ESTATS_FINE_RTT_RW_v0);
        break;

    default:
        return;
        break;
    }

    if (v6) {
        status = SetPerTcp6ConnectionEStats((PMIB_TCP6ROW)row, type,
            rw, 0, size, 0);
    }
    else {
        status = SetPerTcpConnectionEStats((PMIB_TCPROW)row, type,
            rw, 0, size, 0);
    }

    if (status != NO_ERROR) {
        if (v6)
            wprintf(L"\nSetPerTcp6ConnectionEStats %s %s failed. status = %d",
                estatsTypeNames[type], enable ? L"enabled" : L"disabled",
                status);
        else
            wprintf(L"\nSetPerTcpConnectionEStats %s %s failed. status = %d",
                estatsTypeNames[type], enable ? L"enabled" : L"disabled",
                status);
    }
}

//
// Toggle all Estats for a TCP connection.
//
void ToggleAllEstats(void* row, bool enable, bool v6)
{
    ToggleEstat(row, TcpConnectionEstatsData, enable, v6);
    ToggleEstat(row, TcpConnectionEstatsSndCong, enable, v6);
    ToggleEstat(row, TcpConnectionEstatsPath, enable, v6);
    ToggleEstat(row, TcpConnectionEstatsSendBuff, enable, v6);
    ToggleEstat(row, TcpConnectionEstatsRec, enable, v6);
    ToggleEstat(row, TcpConnectionEstatsObsRec, enable, v6);
    ToggleEstat(row, TcpConnectionEstatsBandwidth, enable, v6);
    ToggleEstat(row, TcpConnectionEstatsFineRtt, enable, v6);
}

//
// Call GetPerTcp6ConnectionEStats or GetPerTcpConnectionEStats.
//
ULONG GetConnectionEStats(void* row, TCP_ESTATS_TYPE type, PUCHAR rw, ULONG rwSize, bool v6, PUCHAR ros, ULONG rosSize, PUCHAR rod, ULONG rodSize)
{
    if (v6) {
        return GetPerTcp6ConnectionEStats((PMIB_TCP6ROW)row,
            type,
            rw, 0, rwSize,
            ros, 0, rosSize,
            rod, 0, rodSize);
    }
    else {
        return GetPerTcpConnectionEStats((PMIB_TCPROW)row,
            type,
            rw, 0, rwSize,
            ros, 0, rosSize,
            rod, 0, rodSize);
    }
}

//
// Dump the supplied Estate type on the given TCP connection row.
//
void GetAndOutputEstats(void* row, TCP_ESTATS_TYPE type, bool v6)
{
    ULONG rosSize = 0, rodSize = 0;
    ULONG winStatus;
    PUCHAR ros = NULL, rod = NULL;

    PTCP_ESTATS_SYN_OPTS_ROS_v0 synOptsRos = { 0 };
    PTCP_ESTATS_DATA_ROD_v0 dataRod = { 0 };
    PTCP_ESTATS_SND_CONG_ROD_v0 sndCongRod = { 0 };
    PTCP_ESTATS_SND_CONG_ROS_v0 sndCongRos = { 0 };
    PTCP_ESTATS_PATH_ROD_v0 pathRod = { 0 };
    PTCP_ESTATS_SEND_BUFF_ROD_v0 sndBuffRod = { 0 };
    PTCP_ESTATS_REC_ROD_v0 recRod = { 0 };
    PTCP_ESTATS_OBS_REC_ROD_v0 obsRecRod = { 0 };
    PTCP_ESTATS_BANDWIDTH_ROD_v0 bandwidthRod = { 0 };
    PTCP_ESTATS_FINE_RTT_ROD_v0 fineRttRod = { 0 };

    switch (type) {
    case TcpConnectionEstatsSynOpts:
        rosSize = sizeof(TCP_ESTATS_SYN_OPTS_ROS_v0);
        break;

    case TcpConnectionEstatsData:
        rodSize = sizeof(TCP_ESTATS_DATA_ROD_v0);
        break;

    case TcpConnectionEstatsSndCong:
        rodSize = sizeof(TCP_ESTATS_SND_CONG_ROD_v0);
        rosSize = sizeof(TCP_ESTATS_SND_CONG_ROS_v0);
        break;

    case TcpConnectionEstatsPath:
        rodSize = sizeof(TCP_ESTATS_PATH_ROD_v0);
        break;

    case TcpConnectionEstatsSendBuff:
        rodSize = sizeof(TCP_ESTATS_SEND_BUFF_ROD_v0);
        break;

    case TcpConnectionEstatsRec:
        rodSize = sizeof(TCP_ESTATS_REC_ROD_v0);
        break;

    case TcpConnectionEstatsObsRec:
        rodSize = sizeof(TCP_ESTATS_OBS_REC_ROD_v0);
        break;

    case TcpConnectionEstatsBandwidth:
        rodSize = sizeof(TCP_ESTATS_BANDWIDTH_ROD_v0);
        break;

    case TcpConnectionEstatsFineRtt:
        rodSize = sizeof(TCP_ESTATS_FINE_RTT_ROD_v0);
        break;

    default:
        wprintf(L"\nCannot get type %d", (int)type);
        return;
        break;
    }

    if (rosSize != 0) {
        ros = (PUCHAR)malloc(rosSize);
        if (ros == NULL) {
            wprintf(L"\nOut of memory");
            return;
        }
        else
            memset(ros, 0, rosSize); // zero the buffer
    }
    if (rodSize != 0) {
        rod = (PUCHAR)malloc(rodSize);
        if (rod == NULL) {
            free(ros);
            wprintf(L"\nOut of memory");
            return;
        }
        else
            memset(rod, 0, rodSize); // zero the buffer
    }

    TCP_ESTATS_DATA_RW_v0 dataRw = { 0 };
    TCP_ESTATS_SND_CONG_RW_v0 sndCongRw = { 0 };
    TCP_ESTATS_PATH_RW_v0 pathRw = { 0 };
    TCP_ESTATS_SEND_BUFF_RW_v0 sndBuffRw = { 0 };
    TCP_ESTATS_REC_RW_v0 recRw = { 0 };
    TCP_ESTATS_OBS_REC_RW_v0 obsRecRw = { 0 };
    TCP_ESTATS_BANDWIDTH_RW_v0 bandwidthRw = { 0 };
    TCP_ESTATS_FINE_RTT_RW_v0 fineRttRw = { 0 };
    BOOLEAN RwEnableCollection{ FALSE };

    switch (type) {
    case TcpConnectionEstatsData:
        winStatus = GetConnectionEStats(row, type, (PUCHAR)&dataRw, sizeof(TCP_ESTATS_DATA_RW_v0), v6, ros, rosSize, rod, rodSize);
        RwEnableCollection = dataRw.EnableCollection;
        break;

    case TcpConnectionEstatsSndCong:
        winStatus = GetConnectionEStats(row, type, (PUCHAR)&sndCongRw, sizeof(TCP_ESTATS_SND_CONG_RW_v0), v6, ros, rosSize, rod, rodSize);
        RwEnableCollection = sndCongRw.EnableCollection;
        break;

    case TcpConnectionEstatsPath:
        winStatus = GetConnectionEStats(row, type, (PUCHAR)&pathRw, sizeof(TCP_ESTATS_PATH_RW_v0), v6, ros, rosSize, rod, rodSize);
        RwEnableCollection = pathRw.EnableCollection;
        break;

    case TcpConnectionEstatsSendBuff:
        winStatus = GetConnectionEStats(row, type, (PUCHAR)&sndBuffRw, sizeof(TCP_ESTATS_SEND_BUFF_RW_v0), v6, ros, rosSize, rod, rodSize);
        RwEnableCollection = sndBuffRw.EnableCollection;
        break;

    case TcpConnectionEstatsRec:
        winStatus = GetConnectionEStats(row, type, (PUCHAR)&recRw, sizeof(TCP_ESTATS_REC_RW_v0), v6, ros, rosSize, rod, rodSize);
        RwEnableCollection = recRw.EnableCollection;
        break;

    case TcpConnectionEstatsObsRec:
        winStatus = GetConnectionEStats(row, type, (PUCHAR)&obsRecRw, sizeof(TCP_ESTATS_OBS_REC_RW_v0), v6, ros, rosSize, rod, rodSize);
        RwEnableCollection = obsRecRw.EnableCollection;
        break;

    case TcpConnectionEstatsBandwidth:
        winStatus = GetConnectionEStats(row, type, (PUCHAR)&bandwidthRw, sizeof(TCP_ESTATS_BANDWIDTH_RW_v0), v6, ros, rosSize, rod, rodSize);
        RwEnableCollection = bandwidthRw.EnableCollectionOutbound && bandwidthRw.EnableCollectionInbound;
        break;

    case TcpConnectionEstatsFineRtt:
        winStatus = GetConnectionEStats(row, type, (PUCHAR)&fineRttRw, sizeof(TCP_ESTATS_FINE_RTT_RW_v0), v6, ros, rosSize, rod, rodSize);
        RwEnableCollection = fineRttRw.EnableCollection;
        break;

    default:
        winStatus = GetConnectionEStats(row, type, NULL, v6, 0, ros, rosSize, rod, rodSize);
        break;
    }

    if (!RwEnableCollection) {
        if (v6)
            wprintf(L"\nGetPerTcp6ConnectionEStats %s failed. Rw.EnableCollection == FALSE", estatsTypeNames[type]);
        else
            wprintf(L"\nGetPerTcpConnectionEStats %s failed. Rw.EnableCollection == FALSE", estatsTypeNames[type]);
        return;
    }

    if (winStatus != NO_ERROR) {
        if (v6)
            wprintf(L"\nGetPerTcp6ConnectionEStats %s failed. status = %d",
                estatsTypeNames[type],
                winStatus);
        else
            wprintf(L"\nGetPerTcpConnectionEStats %s failed. status = %d",
                estatsTypeNames[type],
                winStatus);
    }
    else {
        switch (type) {
        case TcpConnectionEstatsSynOpts:
            synOptsRos = (PTCP_ESTATS_SYN_OPTS_ROS_v0)ros;
            wprintf(L"\nSyn Opts");
            wprintf(L"\nActive Open:    %s",
                synOptsRos->ActiveOpen ? L"Yes" : L"No");
            wprintf(L"\nMss Received:   %u", synOptsRos->MssRcvd);
            wprintf(L"\nMss Sent        %u", synOptsRos->MssSent);
            break;

        case TcpConnectionEstatsData:
            dataRod = (PTCP_ESTATS_DATA_ROD_v0)rod;
            wprintf(L"\n\nData");
            wprintf(L"\nBytes Out:   %lu", dataRod->DataBytesOut);
            wprintf(L"\nSegs Out:    %lu", dataRod->DataSegsOut);
            wprintf(L"\nBytes In:    %lu", dataRod->DataBytesIn);
            wprintf(L"\nSegs In:     %lu", dataRod->DataSegsIn);
            wprintf(L"\nSegs Out:    %u", dataRod->SegsOut);
            wprintf(L"\nSegs In:     %u", dataRod->SegsIn);
            wprintf(L"\nSoft Errors: %u", dataRod->SoftErrors);
            wprintf(L"\nSoft Error Reason: %u", dataRod->SoftErrorReason);
            wprintf(L"\nSnd Una:     %u", dataRod->SndUna);
            wprintf(L"\nSnd Nxt:     %u", dataRod->SndNxt);
            wprintf(L"\nSnd Max:     %u", dataRod->SndMax);
            wprintf(L"\nBytes Acked: %lu", dataRod->ThruBytesAcked);
            wprintf(L"\nRcv Nxt:     %u", dataRod->RcvNxt);
            wprintf(L"\nBytes Rcv:   %lu", dataRod->ThruBytesReceived);
            break;

        case TcpConnectionEstatsSndCong:
            sndCongRod = (PTCP_ESTATS_SND_CONG_ROD_v0)rod;
            sndCongRos = (PTCP_ESTATS_SND_CONG_ROS_v0)ros;
            wprintf(L"\n\nSnd Cong");
            wprintf(L"\nTrans Rwin:       %u", sndCongRod->SndLimTransRwin);
            wprintf(L"\nLim Time Rwin:    %u", sndCongRod->SndLimTimeRwin);
            wprintf(L"\nLim Bytes Rwin:   %u", sndCongRod->SndLimBytesRwin);
            wprintf(L"\nLim Trans Cwnd:   %u", sndCongRod->SndLimTransCwnd);
            wprintf(L"\nLim Time Cwnd:    %u", sndCongRod->SndLimTimeCwnd);
            wprintf(L"\nLim Bytes Cwnd:   %u", sndCongRod->SndLimBytesCwnd);
            wprintf(L"\nLim Trans Snd:    %u", sndCongRod->SndLimTransSnd);
            wprintf(L"\nLim Time Snd:     %u", sndCongRod->SndLimTimeSnd);
            wprintf(L"\nLim Bytes Snd:    %u", sndCongRod->SndLimBytesSnd);
            wprintf(L"\nSlow Start:       %u", sndCongRod->SlowStart);
            wprintf(L"\nCong Avoid:       %u", sndCongRod->CongAvoid);
            wprintf(L"\nOther Reductions: %u", sndCongRod->OtherReductions);
            wprintf(L"\nCur Cwnd:         %u", sndCongRod->CurCwnd);
            wprintf(L"\nMax Ss Cwnd:      %u", sndCongRod->MaxSsCwnd);
            wprintf(L"\nMax Ca Cwnd:      %u", sndCongRod->MaxCaCwnd);
            wprintf(L"\nCur Ss Thresh:    0x%x (%u)", sndCongRod->CurSsthresh,
                sndCongRod->CurSsthresh);
            wprintf(L"\nMax Ss Thresh:    0x%x (%u)", sndCongRod->MaxSsthresh,
                sndCongRod->MaxSsthresh);
            wprintf(L"\nMin Ss Thresh:    0x%x (%u)", sndCongRod->MinSsthresh,
                sndCongRod->MinSsthresh);
            wprintf(L"\nLim Cwnd:         0x%x (%u)", sndCongRos->LimCwnd,
                sndCongRos->LimCwnd);
            break;

        case TcpConnectionEstatsPath:
            pathRod = (PTCP_ESTATS_PATH_ROD_v0)rod;
            wprintf(L"\n\nPath");
            wprintf(L"\nFast Retran:         %u", pathRod->FastRetran);
            wprintf(L"\nTimeouts:            %u", pathRod->Timeouts);
            wprintf(L"\nSubsequent Timeouts: %u", pathRod->SubsequentTimeouts);
            wprintf(L"\nCur Timeout Count:   %u", pathRod->CurTimeoutCount);
            wprintf(L"\nAbrupt Timeouts:     %u", pathRod->AbruptTimeouts);
            wprintf(L"\nPkts Retrans:        %u", pathRod->PktsRetrans);
            wprintf(L"\nBytes Retrans:       %u", pathRod->BytesRetrans);
            wprintf(L"\nDup Acks In:         %u", pathRod->DupAcksIn);
            wprintf(L"\nSacksRcvd:           %u", pathRod->SacksRcvd);
            wprintf(L"\nSack Blocks Rcvd:    %u", pathRod->SackBlocksRcvd);
            wprintf(L"\nCong Signals:        %u", pathRod->CongSignals);
            wprintf(L"\nPre Cong Sum Cwnd:   %u", pathRod->PreCongSumCwnd);
            wprintf(L"\nPre Cong Sum Rtt:    %u", pathRod->PreCongSumRtt);
            wprintf(L"\nPost Cong Sum Rtt:   %u", pathRod->PostCongSumRtt);
            wprintf(L"\nPost Cong Count Rtt: %u", pathRod->PostCongCountRtt);
            wprintf(L"\nEcn Signals:         %u", pathRod->EcnSignals);
            wprintf(L"\nEce Rcvd:            %u", pathRod->EceRcvd);
            wprintf(L"\nSend Stall:          %u", pathRod->SendStall);
            wprintf(L"\nQuench Rcvd:         %u", pathRod->QuenchRcvd);
            wprintf(L"\nRetran Thresh:       %u", pathRod->RetranThresh);
            wprintf(L"\nSnd Dup Ack Episodes:  %u", pathRod->SndDupAckEpisodes);
            wprintf(L"\nSum Bytes Reordered: %u", pathRod->SumBytesReordered);
            wprintf(L"\nNon Recov Da:        %u", pathRod->NonRecovDa);
            wprintf(L"\nNon Recov Da Episodes: %u", pathRod->NonRecovDaEpisodes);
            wprintf(L"\nAck After Fr:        %u", pathRod->AckAfterFr);
            wprintf(L"\nDsack Dups:          %u", pathRod->DsackDups);
            wprintf(L"\nSample Rtt:          0x%x (%u)", pathRod->SampleRtt,
                pathRod->SampleRtt);
            wprintf(L"\nSmoothed Rtt:        %u", pathRod->SmoothedRtt);
            wprintf(L"\nRtt Var:             %u", pathRod->RttVar);
            wprintf(L"\nMax Rtt:             %u", pathRod->MaxRtt);
            wprintf(L"\nMin Rtt:             0x%x (%u)", pathRod->MinRtt,
                pathRod->MinRtt);
            wprintf(L"\nSum Rtt:             %u", pathRod->SumRtt);
            wprintf(L"\nCount Rtt:           %u", pathRod->CountRtt);
            wprintf(L"\nCur Rto:             %u", pathRod->CurRto);
            wprintf(L"\nMax Rto:             %u", pathRod->MaxRto);
            wprintf(L"\nMin Rto:             %u", pathRod->MinRto);
            wprintf(L"\nCur Mss:             %u", pathRod->CurMss);
            wprintf(L"\nMax Mss:             %u", pathRod->MaxMss);
            wprintf(L"\nMin Mss:             %u", pathRod->MinMss);
            wprintf(L"\nSpurious Rto:        %u", pathRod->SpuriousRtoDetections);
            break;

        case TcpConnectionEstatsSendBuff:
            sndBuffRod = (PTCP_ESTATS_SEND_BUFF_ROD_v0)rod;
            wprintf(L"\n\nSend Buff");
            wprintf(L"\nCur Retx Queue:   %u", sndBuffRod->CurRetxQueue);
            wprintf(L"\nMax Retx Queue:   %u", sndBuffRod->MaxRetxQueue);
            wprintf(L"\nCur App W Queue:  %u", sndBuffRod->CurAppWQueue);
            wprintf(L"\nMax App W Queue:  %u", sndBuffRod->MaxAppWQueue);
            break;

        case TcpConnectionEstatsRec:
            recRod = (PTCP_ESTATS_REC_ROD_v0)rod;
            wprintf(L"\n\nRec");
            wprintf(L"\nCur Rwin Sent:   0x%x (%u)", recRod->CurRwinSent,
                recRod->CurRwinSent);
            wprintf(L"\nMax Rwin Sent:   0x%x (%u)", recRod->MaxRwinSent,
                recRod->MaxRwinSent);
            wprintf(L"\nMin Rwin Sent:   0x%x (%u)", recRod->MinRwinSent,
                recRod->MinRwinSent);
            wprintf(L"\nLim Rwin:        0x%x (%u)", recRod->LimRwin,
                recRod->LimRwin);
            wprintf(L"\nDup Acks:        %u", recRod->DupAckEpisodes);
            wprintf(L"\nDup Acks Out:    %u", recRod->DupAcksOut);
            wprintf(L"\nCe Rcvd:         %u", recRod->CeRcvd);
            wprintf(L"\nEcn Send:        %u", recRod->EcnSent);
            wprintf(L"\nEcn Nonces Rcvd: %u", recRod->EcnNoncesRcvd);
            wprintf(L"\nCur Reasm Queue: %u", recRod->CurReasmQueue);
            wprintf(L"\nMax Reasm Queue: %u", recRod->MaxReasmQueue);
            wprintf(L"\nCur App R Queue: %u", recRod->CurAppRQueue);
            wprintf(L"\nMax App R Queue: %u", recRod->MaxAppRQueue);
            wprintf(L"\nWin Scale Sent:  0x%.2x", recRod->WinScaleSent);
            break;

        case TcpConnectionEstatsObsRec:
            obsRecRod = (PTCP_ESTATS_OBS_REC_ROD_v0)rod;
            wprintf(L"\n\nObs Rec");
            wprintf(L"\nCur Rwin Rcvd:   0x%x (%u)", obsRecRod->CurRwinRcvd,
                obsRecRod->CurRwinRcvd);
            wprintf(L"\nMax Rwin Rcvd:   0x%x (%u)", obsRecRod->MaxRwinRcvd,
                obsRecRod->MaxRwinRcvd);
            wprintf(L"\nMin Rwin Rcvd:   0x%x (%u)", obsRecRod->MinRwinRcvd,
                obsRecRod->MinRwinRcvd);
            wprintf(L"\nWin Scale Rcvd:  0x%x (%u)", obsRecRod->WinScaleRcvd,
                obsRecRod->WinScaleRcvd);
            break;

        case TcpConnectionEstatsBandwidth:
            bandwidthRod = (PTCP_ESTATS_BANDWIDTH_ROD_v0)rod;
            wprintf(L"\n\nBandwidth");
            wprintf(L"\nOutbound Bandwidth:   %lu",
                bandwidthRod->OutboundBandwidth);
            wprintf(L"\nInbound Bandwidth:    %lu", bandwidthRod->InboundBandwidth);
            wprintf(L"\nOutbound Instability: %lu",
                bandwidthRod->OutboundInstability);
            wprintf(L"\nInbound Instability:  %lu",
                bandwidthRod->InboundInstability);
            wprintf(L"\nOutbound Bandwidth Peaked: %s",
                bandwidthRod->OutboundBandwidthPeaked ? L"Yes" : L"No");
            wprintf(L"\nInbound Bandwidth Peaked:  %s",
                bandwidthRod->InboundBandwidthPeaked ? L"Yes" : L"No");
            break;

        case TcpConnectionEstatsFineRtt:
            fineRttRod = (PTCP_ESTATS_FINE_RTT_ROD_v0)rod;
            wprintf(L"\n\nFine RTT");
            wprintf(L"\nRtt Var: %u", fineRttRod->RttVar);
            wprintf(L"\nMax Rtt: %u", fineRttRod->MaxRtt);
            wprintf(L"\nMin Rtt: 0x%x (%u) ", fineRttRod->MinRtt,
                fineRttRod->MinRtt);
            wprintf(L"\nSum Rtt: %u", fineRttRod->SumRtt);
            break;

        default:
            wprintf(L"\nCannot get type %d", type);
            break;
        }
    }

    free(ros);
    free(rod);
}
```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table">MIB_TCP6TABLE</a>



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