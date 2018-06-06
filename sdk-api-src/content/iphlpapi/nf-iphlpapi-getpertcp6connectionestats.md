---
UID: NF:iphlpapi.GetPerTcp6ConnectionEStats
title: GetPerTcp6ConnectionEStats function
author: windows-sdk-content
description: Retrieves extended statistics for an IPv6 TCP connection.
old-location: iphlp\getpertcp6connectionestats.htm
old-project: IpHlp
ms.assetid: 291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetPerTcp6ConnectionEStats, GetPerTcp6ConnectionEStats function [IP Helper], TcpConnectionEstatsBandwidth, TcpConnectionEstatsData, TcpConnectionEstatsFineRtt, TcpConnectionEstatsObsRec, TcpConnectionEstatsPath, TcpConnectionEstatsRec, TcpConnectionEstatsSendBuff, TcpConnectionEstatsSndCong, TcpConnectionEstatsSynOpts, iphlp.getpertcp6connectionestats, iphlpapi/GetPerTcp6ConnectionEStats
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: NET_ADDRESS_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetPerTcp6ConnectionEStats
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetPerTcp6ConnectionEStats function


## -description


The 
<b>GetPerTcp6ConnectionEStats</b> function retrieves extended statistics for an IPv6 TCP connection.


## -parameters




### -param Row

A pointer to a <a href="https://msdn.microsoft.com/b3e9eda5-5e86-4790-8b1b-ca9bae44b502">MIB_TCP6ROW</a> structure for an IPv6 TCP connection. 


### -param EstatsType

The type of extended statistics for TCP requested. This parameter determines the data and format of information that is returned in the <i>Rw</i>, <i>Rod</i>, and <i>Ros</i> parameters if the call is successful.

This parameter can be one of the values from the <a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a> enumeration type defined in the <i>Tcpestats.h</i> header file. 

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

If the <i>Ros</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Ros</i> parameter should contain a <a href="https://msdn.microsoft.com/e183b23c-ce87-4818-b6d6-2305a3aa345d">TCP_ESTATS_SYN_OPTS_ROS_v0</a> structure.

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

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="https://msdn.microsoft.com/823cea66-f719-40f6-82bd-572623188446">TCP_ESTATS_DATA_RW_v0</a> structure. 

If extended data transfer information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="https://msdn.microsoft.com/1e896660-10dd-471a-b4ae-116caa7a9d48">TCP_ESTATS_DATA_ROD_v0</a> structure. 

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

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="https://msdn.microsoft.com/7fc7fb6a-4486-450f-b60e-8cf07b33c79a">TCP_ESTATS_SND_CONG_RW_v0</a> structure. 

If the <i>Ros</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Ros</i> parameter should contain a <a href="https://msdn.microsoft.com/4c92af92-ed51-4548-873f-b25207ea46dc">TCP_ESTATS_SND_CONG_ROS_v0</a> structure.

If sender congestion information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="https://msdn.microsoft.com/5eb2d1c6-d4ba-4038-b598-ead517679ae7">TCP_ESTATS_SND_CONG_ROD_v0</a> structure. 

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

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="https://msdn.microsoft.com/460ad710-06aa-490a-9bac-5a8c731687e9">TCP_ESTATS_PATH_RW_v0</a> structure. 

If extended path measurement information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="https://msdn.microsoft.com/35ed2a10-caac-4004-80ac-f62c3880f5de">TCP_ESTATS_PATH_ROD_v0</a> structure. 

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

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="https://msdn.microsoft.com/1bc88d95-24d2-4ca3-9f4a-298d5c08f4de">TCP_ESTATS_SEND_BUFF_RW_v0</a> structure. 

If extended output-queuing information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="https://msdn.microsoft.com/7cda7378-95e4-4f1d-88b3-27974fedec83">TCP_ESTATS_SEND_BUFF_ROD_v0</a> structure. 

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

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="https://msdn.microsoft.com/e780ae7b-30c6-4890-8a8b-9e0b2739c176">TCP_ESTATS_REC_RW_v0</a> structure. 

If extended local-receiver information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="https://msdn.microsoft.com/1481f108-1ea3-4952-9131-8b15e373d83e">TCP_ESTATS_REC_ROD_v0</a> structure. 

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

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="https://msdn.microsoft.com/91c2d5d9-3198-42a7-abf7-077281b491f2">TCP_ESTATS_OBS_REC_RW_v0</a> structure. 

If extended remote-receiver information was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="https://msdn.microsoft.com/f790e107-0db3-4691-98fc-378518b04a8a">TCP_ESTATS_OBS_REC_ROD_v0</a> structure. 

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

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="https://msdn.microsoft.com/a9bf5ad3-a8db-4194-8e47-5a7409391f4c">TCP_ESTATS_BANDWIDTH_RW_v0</a> structure. 

If bandwidth estimation statistics was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="https://msdn.microsoft.com/330d06a2-9966-4e2b-b1bd-44c0f1b9416d">TCP_ESTATS_BANDWIDTH_ROD_v0</a> structure. 

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

If the <i>Rw</i> parameter was not <b>NULL</b> and the function succeeds, the buffer pointed to by the <i>Rw</i> parameter should contain a <a href="https://msdn.microsoft.com/35834c9a-2896-4c11-aef7-c55af7f6fef3">TCP_ESTATS_FINE_RTT_RW_v0</a> structure. 

If fine-grained RTT estimation statistics was enabled  for this TCP connection, the <i>Rod</i> parameter was not <b>NULL</b>, and the function succeeds, the buffer pointed to by the <i>Rod</i> parameter should contain a <a href="https://msdn.microsoft.com/e33cd21f-1ec8-4715-a5e1-431a8a7e61df">TCP_ESTATS_FINE_RTT_ROD_v0</a> structure. 

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

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


The <b>GetPerTcp6ConnectionEStats</b> function retrieves extended statistics for the IPv6 TCP connection passed in the <i>Row</i> parameter. The type of extended statistics that is retrieved is specified in the <i>EstatsType</i> parameter. Extended statistics on this TCP connection must have previously been enabled by calls to the <a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a> function for all <a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a> values except when <b>TcpConnectionEstatsSynOpts</b> is passed in the <i>EstatsType</i> parameter. 

The <a href="https://msdn.microsoft.com/77150609-d06d-4492-bbd7-21eecd825bde">GetTcp6Table</a> function is used to retrieve the IPv6 TCP connection table on the local computer. This function returns a <a href="https://msdn.microsoft.com/62bb8544-0a0a-40b5-92cf-9631c9a9987c">MIB_TCP6TABLE</a> structure that contain an array of <a href="https://msdn.microsoft.com/b3e9eda5-5e86-4790-8b1b-ca9bae44b502">MIB_TCP6ROW</a> entries. The <i>Row</i> parameter passed to the <b>GetPerTcp6ConnectionEStats</b> function must be an entry for an existing IPv6 TCP connection.

The only version of TCP connection statistics currently supported is version zero. So the <i>RwVersion</i>, <i>RosVersion</i>, and <i>RodVersion</i> parameters passed to <b>GetPerTcp6ConnectionEStats</b> should be set to 0.

For information on extended TCP statistics on an IPv4 connection, see the <a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a> and <a href="https://msdn.microsoft.com/96d838ca-69e3-4a73-b969-3e6e810a0a69">SetPerTcpConnectionEStats</a> functions.

The <a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a> function can only be called by a user logged on as a member of the Administrators group. If <b>SetPerTcp6ConnectionEStats</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



An application that uses the <b>GetPerTcp6ConnectionEStats</b> function to retrieve extended statistics for an IPv6 TCP connection must check that the previous call to the <a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a> function to enabled extended statistics returned with success. If the <b>SetPerTcp6ConnectionEStats</b> function to enable extended statistics failed, subsequent calls to the <b>GetPerTcp6ConnectionEStats</b> will still return numbers in the returned structures. However the returned numbers are meaningless random data and don't represent extended TCP statistics. This behavior can be observed by running the example below as both an administrator and a normal user.


#### Examples

The following example retrieves the TCP extended statistics for an IPv4 and IPv6 TCP connection and prints values from the returned data.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Need to link with Iphlpapi.lib and Ws2_32.lib
// Need to run as administrator

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include &lt;windows.h&gt;
#include &lt;winsock2.h&gt;
#include &lt;Ws2tcpip.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;Tcpestats.h&gt;
#include &lt;stdlib.h&gt;
#include &lt;stdio.h&gt;

// Need to link with Iphlpapi.lib
#pragma comment(lib, "iphlpapi.lib")

// Need to link with Ws2_32.lib
#pragma comment(lib, "ws2_32.lib")

// An array of name for the TCP_ESTATS_TYPE enum values
// The names values must match the enum values
wchar_t *estatsTypeNames[] = {
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
void ToggleAllEstats(void *row, bool enable, bool v6);

// Dump the supplied Estate type data on the given TCP connection row
void GetAndOutputEstats(void *row, TCP_ESTATS_TYPE type, bool v6);

//
void GetAllEstats(void *row, bool v6);

// Creates a TCP server and client socket on the loopback address.
// Binds the server socket to a port.
// Establishes a client TCP connection to the server 
int CreateTcpConnection(bool v6, SOCKET * serviceSocket, SOCKET * clientSocket,
                        SOCKET * acceptSocket, u_short * serverPort,
                        u_short * clientPort);

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
    void *serverConnectRow, *clientConnectRow = NULL;
    bool bWSAStartup = false;

    char *buff = (char *) malloc(1000);
    if (buff == NULL) {
        wprintf(L"\nFailed to allocate memory.");
        goto bail;
    }

    if (v6) {
        serverConnectRow = &amp;server6ConnectRow;
        clientConnectRow = &amp;client6ConnectRow;
    } else {
        serverConnectRow = &amp;server4ConnectRow;
        clientConnectRow = &amp;client4ConnectRow;
    }

    UINT winStatus;
    int sockStatus;
    u_short serverPort, clientPort;

    //
    // Initialize Winsock.
    //
    WSADATA wsaData;
    winStatus = WSAStartup(MAKEWORD(2, 2), &amp;wsaData);
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
        CreateTcpConnection(v6, &amp;serviceSocket, &amp;clientSocket, &amp;acceptSocket,
                            &amp;serverPort, &amp;clientPort);
    if (winStatus != ERROR_SUCCESS) {
        wprintf(L"\nFailed to create TCP connection. Error %d", winStatus);
        goto bail;
    }
    //
    // Obtain MIB_TCPROW corresponding to the TCP connection.
    //
    winStatus = v6 ?
        GetTcp6Row(serverPort, clientPort, MIB_TCP_STATE_ESTAB,
                   (PMIB_TCP6ROW) serverConnectRow) :
        GetTcpRow(serverPort, clientPort, MIB_TCP_STATE_ESTAB,
                  (PMIB_TCPROW) serverConnectRow);
    if (winStatus != ERROR_SUCCESS) {
        wprintf
            (L"\nGetTcpRow failed on the server established connection with %d",
             winStatus);
        goto bail;
    }

    winStatus = v6 ?
        GetTcp6Row(clientPort, serverPort, MIB_TCP_STATE_ESTAB,
                   (PMIB_TCP6ROW) clientConnectRow) :
        GetTcpRow(clientPort, serverPort, MIB_TCP_STATE_ESTAB,
                  (PMIB_TCPROW) clientConnectRow);
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
    sockStatus = send(clientSocket, buff, (int) (1000 * sizeof (char)), 0);
    if (sockStatus == SOCKET_ERROR) {
        wprintf(L"\nFailed to send from client to server %d",
                WSAGetLastError());
    } else {
        sockStatus = recv(acceptSocket, buff, (int) (1000 * sizeof (char)), 0);
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
                        SOCKET * serviceSocket,
                        SOCKET * clientSocket,
                        SOCKET * acceptSocket,
                        u_short * serverPort, u_short * clientPort)
{
    INT status;
    ADDRINFOW hints, *localhost = NULL;
    wchar_t *loopback;
    loopback = v6 ? L"::1" : L"127.0.0.1";
    int aiFamily = v6 ? AF_INET6 : AF_INET;

    *serviceSocket = INVALID_SOCKET;
    *clientSocket = INVALID_SOCKET;
    *acceptSocket = INVALID_SOCKET;

    ZeroMemory(&amp;hints, sizeof (hints));
    hints.ai_family = aiFamily;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;

    status = GetAddrInfoW(loopback, L"", &amp;hints, &amp;localhost);
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
        bind(*serviceSocket, localhost-&gt;ai_addr, (int) localhost-&gt;ai_addrlen);
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
    int nameLen = sizeof (SOCKADDR_STORAGE);
    status = getsockname(*serviceSocket,
                         (sockaddr *) &amp; serverSockName, &amp;nameLen);
    if (status == SOCKET_ERROR) {
        wprintf(L"\ngetsockname failed %d", WSAGetLastError());
        goto bail;
    }
    if (v6) {
        *serverPort = ((sockaddr_in6 *) (&amp;serverSockName))-&gt;sin6_port;
    } else {
        *serverPort = ((sockaddr_in *) (&amp;serverSockName))-&gt;sin_port;
    }

    status = listen(*serviceSocket, SOMAXCONN);
    if (status == SOCKET_ERROR) {
        wprintf(L"\nFailed to listen on server socket. Error %d",
                WSAGetLastError());
        goto bail;
    }

    status =
        connect(*clientSocket, (sockaddr *) &amp; serverSockName,
                (int) sizeof (SOCKADDR_STORAGE));
    if (status == SOCKET_ERROR) {
        wprintf(L"\nCould not connect client and server sockets %d",
                WSAGetLastError());
        goto bail;
    }

    status = getsockname(*clientSocket,
                         (sockaddr *) &amp; clientSockName, &amp;nameLen);
    if (status == SOCKET_ERROR) {
        wprintf(L"\ngetsockname failed %d", WSAGetLastError());
        goto bail;
    }
    if (v6) {
        *clientPort = ((sockaddr_in6 *) (&amp;clientSockName))-&gt;sin6_port;
    } else {
        *clientPort = ((sockaddr_in *) (&amp;clientSockName))-&gt;sin_port;
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

void GetAllEstats(void *row, bool v6)
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

    status = GetTcpTable(tcpTable, &amp;size, TRUE);
    if (status != ERROR_INSUFFICIENT_BUFFER) {
        return status;
    }

    tcpTable = (PMIB_TCPTABLE) malloc(size);
    if (tcpTable == NULL) {
        return ERROR_OUTOFMEMORY;
    }

    status = GetTcpTable(tcpTable, &amp;size, TRUE);
    if (status != ERROR_SUCCESS) {
        free(tcpTable);
        return status;
    }

    for (i = 0; i &lt; tcpTable-&gt;dwNumEntries; i++) {
        tcpRowIt = &amp;tcpTable-&gt;table[i];
        if (tcpRowIt-&gt;dwLocalPort == (DWORD) localPort &amp;&amp;
            tcpRowIt-&gt;dwRemotePort == (DWORD) remotePort &amp;&amp;
            tcpRowIt-&gt;State == state) {
            connectionFound = TRUE;
            *row = *tcpRowIt;
            break;
        }
    }

    free(tcpTable);

    if (connectionFound) {
        return ERROR_SUCCESS;
    } else {
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

    status = GetTcp6Table(tcp6Table, &amp;size, TRUE);
    if (status != ERROR_INSUFFICIENT_BUFFER) {
        return status;
    }

    tcp6Table = (PMIB_TCP6TABLE) malloc(size);
    if (tcp6Table == NULL) {
        return ERROR_OUTOFMEMORY;
    }

    status = GetTcp6Table(tcp6Table, &amp;size, TRUE);
    if (status != ERROR_SUCCESS) {
        free(tcp6Table);
        return status;
    }

    for (i = 0; i &lt; tcp6Table-&gt;dwNumEntries; i++) {
        tcp6RowIt = &amp;tcp6Table-&gt;table[i];
        if (tcp6RowIt-&gt;dwLocalPort == (DWORD) localPort &amp;&amp;
            tcp6RowIt-&gt;dwRemotePort == (DWORD) remotePort &amp;&amp;
            tcp6RowIt-&gt;State == state) {
            connectionFound = TRUE;
            *row = *tcp6RowIt;
            break;
        }
    }

    free(tcp6Table);

    if (connectionFound) {
        return ERROR_SUCCESS;
    } else {
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
        rw = (PUCHAR) &amp; dataRw;
        size = sizeof (TCP_ESTATS_DATA_RW_v0);
        break;

    case TcpConnectionEstatsSndCong:
        sndRw.EnableCollection = enable;
        rw = (PUCHAR) &amp; sndRw;
        size = sizeof (TCP_ESTATS_SND_CONG_RW_v0);
        break;

    case TcpConnectionEstatsPath:
        pathRw.EnableCollection = enable;
        rw = (PUCHAR) &amp; pathRw;
        size = sizeof (TCP_ESTATS_PATH_RW_v0);
        break;

    case TcpConnectionEstatsSendBuff:
        sendBuffRw.EnableCollection = enable;
        rw = (PUCHAR) &amp; sendBuffRw;
        size = sizeof (TCP_ESTATS_SEND_BUFF_RW_v0);
        break;

    case TcpConnectionEstatsRec:
        recRw.EnableCollection = enable;
        rw = (PUCHAR) &amp; recRw;
        size = sizeof (TCP_ESTATS_REC_RW_v0);
        break;

    case TcpConnectionEstatsObsRec:
        obsRecRw.EnableCollection = enable;
        rw = (PUCHAR) &amp; obsRecRw;
        size = sizeof (TCP_ESTATS_OBS_REC_RW_v0);
        break;

    case TcpConnectionEstatsBandwidth:
        bandwidthRw.EnableCollectionInbound = operation;
        bandwidthRw.EnableCollectionOutbound = operation;
        rw = (PUCHAR) &amp; bandwidthRw;
        size = sizeof (TCP_ESTATS_BANDWIDTH_RW_v0);
        break;

    case TcpConnectionEstatsFineRtt:
        fineRttRw.EnableCollection = enable;
        rw = (PUCHAR) &amp; fineRttRw;
        size = sizeof (TCP_ESTATS_FINE_RTT_RW_v0);
        break;

    default:
        return;
        break;
    }

    if (v6) {
        status = SetPerTcp6ConnectionEStats((PMIB_TCP6ROW) row, type,
                                            rw, 0, size, 0);
    } else {
        status = SetPerTcpConnectionEStats((PMIB_TCPROW) row, type,
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
void ToggleAllEstats(void *row, bool enable, bool v6)
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
// Dump the supplied Estate type on the given TCP connection row.
//
void GetAndOutputEstats(void *row, TCP_ESTATS_TYPE type, bool v6)
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
        rosSize = sizeof (TCP_ESTATS_SYN_OPTS_ROS_v0);
        break;

    case TcpConnectionEstatsData:
        rodSize = sizeof (TCP_ESTATS_DATA_ROD_v0);
        break;

    case TcpConnectionEstatsSndCong:
        rodSize = sizeof (TCP_ESTATS_SND_CONG_ROD_v0);
        rosSize = sizeof (TCP_ESTATS_SND_CONG_ROS_v0);
        break;

    case TcpConnectionEstatsPath:
        rodSize = sizeof (TCP_ESTATS_PATH_ROD_v0);
        break;

    case TcpConnectionEstatsSendBuff:
        rodSize = sizeof (TCP_ESTATS_SEND_BUFF_ROD_v0);
        break;

    case TcpConnectionEstatsRec:
        rodSize = sizeof (TCP_ESTATS_REC_ROD_v0);
        break;

    case TcpConnectionEstatsObsRec:
        rodSize = sizeof (TCP_ESTATS_OBS_REC_ROD_v0);
        break;

    case TcpConnectionEstatsBandwidth:
        rodSize = sizeof (TCP_ESTATS_BANDWIDTH_ROD_v0);
        break;

    case TcpConnectionEstatsFineRtt:
        rodSize = sizeof (TCP_ESTATS_FINE_RTT_ROD_v0);
        break;

    default:
        wprintf(L"\nCannot get type %d", (int) type);
        return;
        break;
    }

    if (rosSize != 0) {
        ros = (PUCHAR) malloc(rosSize);
        if (ros == NULL) {
            wprintf(L"\nOut of memory");
            return;
        }
        else
            memset(ros,0, rosSize); // zero the buffer
    }
    if (rodSize != 0) {
        rod = (PUCHAR) malloc(rodSize);
        if (rod == NULL) {
            free(ros);
            wprintf(L"\nOut of memory");
            return;
        }
        else
            memset(rod,0, rodSize); // zero the buffer
    }

    if (v6) {
        winStatus = GetPerTcp6ConnectionEStats((PMIB_TCP6ROW) row,
                                               type,
                                               NULL, 0, 0,
                                               ros, 0, rosSize,
                                               rod, 0, rodSize);
    } else {
        winStatus = GetPerTcpConnectionEStats((PMIB_TCPROW) row,
                                              type,
                                              NULL, 0, 0,
                                              ros, 0, rosSize, rod, 0, rodSize);
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
        synOptsRos = (PTCP_ESTATS_SYN_OPTS_ROS_v0) ros;
        wprintf(L"\nSyn Opts");
        wprintf(L"\nActive Open:    %s",
                synOptsRos-&gt;ActiveOpen ? L"Yes" : L"No");
        wprintf(L"\nMss Received:   %u", synOptsRos-&gt;MssRcvd);
        wprintf(L"\nMss Sent        %u", synOptsRos-&gt;MssSent);
        break;

    case TcpConnectionEstatsData:
        dataRod = (PTCP_ESTATS_DATA_ROD_v0) rod;
        wprintf(L"\n\nData");
        wprintf(L"\nBytes Out:   %lu", dataRod-&gt;DataBytesOut);
        wprintf(L"\nSegs Out:    %lu", dataRod-&gt;DataSegsOut);
        wprintf(L"\nBytes In:    %lu", dataRod-&gt;DataBytesIn);
        wprintf(L"\nSegs In:     %lu", dataRod-&gt;DataSegsIn);
        wprintf(L"\nSegs Out:    %u", dataRod-&gt;SegsOut);
        wprintf(L"\nSegs In:     %u", dataRod-&gt;SegsIn);
        wprintf(L"\nSoft Errors: %u", dataRod-&gt;SoftErrors);
        wprintf(L"\nSoft Error Reason: %u", dataRod-&gt;SoftErrorReason);
        wprintf(L"\nSnd Una:     %u", dataRod-&gt;SndUna);
        wprintf(L"\nSnd Nxt:     %u", dataRod-&gt;SndNxt);
        wprintf(L"\nSnd Max:     %u", dataRod-&gt;SndMax);
        wprintf(L"\nBytes Acked: %lu", dataRod-&gt;ThruBytesAcked);
        wprintf(L"\nRcv Nxt:     %u", dataRod-&gt;RcvNxt);
        wprintf(L"\nBytes Rcv:   %lu", dataRod-&gt;ThruBytesReceived);
        break;

    case TcpConnectionEstatsSndCong:
        sndCongRod = (PTCP_ESTATS_SND_CONG_ROD_v0) rod;
        sndCongRos = (PTCP_ESTATS_SND_CONG_ROS_v0) ros;
        wprintf(L"\n\nSnd Cong");
        wprintf(L"\nTrans Rwin:       %u", sndCongRod-&gt;SndLimTransRwin);
        wprintf(L"\nLim Time Rwin:    %u", sndCongRod-&gt;SndLimTimeRwin);
        wprintf(L"\nLim Bytes Rwin:   %u", sndCongRod-&gt;SndLimBytesRwin);
        wprintf(L"\nLim Trans Cwnd:   %u", sndCongRod-&gt;SndLimTransCwnd);
        wprintf(L"\nLim Time Cwnd:    %u", sndCongRod-&gt;SndLimTimeCwnd);
        wprintf(L"\nLim Bytes Cwnd:   %u", sndCongRod-&gt;SndLimBytesCwnd);
        wprintf(L"\nLim Trans Snd:    %u", sndCongRod-&gt;SndLimTransSnd);
        wprintf(L"\nLim Time Snd:     %u", sndCongRod-&gt;SndLimTimeSnd);
        wprintf(L"\nLim Bytes Snd:    %u", sndCongRod-&gt;SndLimBytesSnd);
        wprintf(L"\nSlow Start:       %u", sndCongRod-&gt;SlowStart);
        wprintf(L"\nCong Avoid:       %u", sndCongRod-&gt;CongAvoid);
        wprintf(L"\nOther Reductions: %u", sndCongRod-&gt;OtherReductions);
        wprintf(L"\nCur Cwnd:         %u", sndCongRod-&gt;CurCwnd);
        wprintf(L"\nMax Ss Cwnd:      %u", sndCongRod-&gt;MaxSsCwnd);
        wprintf(L"\nMax Ca Cwnd:      %u", sndCongRod-&gt;MaxCaCwnd);
        wprintf(L"\nCur Ss Thresh:    0x%x (%u)", sndCongRod-&gt;CurSsthresh,
                sndCongRod-&gt;CurSsthresh);
        wprintf(L"\nMax Ss Thresh:    0x%x (%u)", sndCongRod-&gt;MaxSsthresh,
                sndCongRod-&gt;MaxSsthresh);
        wprintf(L"\nMin Ss Thresh:    0x%x (%u)", sndCongRod-&gt;MinSsthresh,
                sndCongRod-&gt;MinSsthresh);
        wprintf(L"\nLim Cwnd:         0x%x (%u)", sndCongRos-&gt;LimCwnd,
                sndCongRos-&gt;LimCwnd);
        break;

    case TcpConnectionEstatsPath:
        pathRod = (PTCP_ESTATS_PATH_ROD_v0) rod;
        wprintf(L"\n\nPath");
        wprintf(L"\nFast Retran:         %u", pathRod-&gt;FastRetran);
        wprintf(L"\nTimeouts:            %u", pathRod-&gt;Timeouts);
        wprintf(L"\nSubsequent Timeouts: %u", pathRod-&gt;SubsequentTimeouts);
        wprintf(L"\nCur Timeout Count:   %u", pathRod-&gt;CurTimeoutCount);
        wprintf(L"\nAbrupt Timeouts:     %u", pathRod-&gt;AbruptTimeouts);
        wprintf(L"\nPkts Retrans:        %u", pathRod-&gt;PktsRetrans);
        wprintf(L"\nBytes Retrans:       %u", pathRod-&gt;BytesRetrans);
        wprintf(L"\nDup Acks In:         %u", pathRod-&gt;DupAcksIn);
        wprintf(L"\nSacksRcvd:           %u", pathRod-&gt;SacksRcvd);
        wprintf(L"\nSack Blocks Rcvd:    %u", pathRod-&gt;SackBlocksRcvd);
        wprintf(L"\nCong Signals:        %u", pathRod-&gt;CongSignals);
        wprintf(L"\nPre Cong Sum Cwnd:   %u", pathRod-&gt;PreCongSumCwnd);
        wprintf(L"\nPre Cong Sum Rtt:    %u", pathRod-&gt;PreCongSumRtt);
        wprintf(L"\nPost Cong Sum Rtt:   %u", pathRod-&gt;PostCongSumRtt);
        wprintf(L"\nPost Cong Count Rtt: %u", pathRod-&gt;PostCongCountRtt);
        wprintf(L"\nEcn Signals:         %u", pathRod-&gt;EcnSignals);
        wprintf(L"\nEce Rcvd:            %u", pathRod-&gt;EceRcvd);
        wprintf(L"\nSend Stall:          %u", pathRod-&gt;SendStall);
        wprintf(L"\nQuench Rcvd:         %u", pathRod-&gt;QuenchRcvd);
        wprintf(L"\nRetran Thresh:       %u", pathRod-&gt;RetranThresh);
        wprintf(L"\nSnd Dup Ack Episodes:  %u", pathRod-&gt;SndDupAckEpisodes);
        wprintf(L"\nSum Bytes Reordered: %u", pathRod-&gt;SumBytesReordered);
        wprintf(L"\nNon Recov Da:        %u", pathRod-&gt;NonRecovDa);
        wprintf(L"\nNon Recov Da Episodes: %u", pathRod-&gt;NonRecovDaEpisodes);
        wprintf(L"\nAck After Fr:        %u", pathRod-&gt;AckAfterFr);
        wprintf(L"\nDsack Dups:          %u", pathRod-&gt;DsackDups);
        wprintf(L"\nSample Rtt:          0x%x (%u)", pathRod-&gt;SampleRtt,
                pathRod-&gt;SampleRtt);
        wprintf(L"\nSmoothed Rtt:        %u", pathRod-&gt;SmoothedRtt);
        wprintf(L"\nRtt Var:             %u", pathRod-&gt;RttVar);
        wprintf(L"\nMax Rtt:             %u", pathRod-&gt;MaxRtt);
        wprintf(L"\nMin Rtt:             0x%x (%u)", pathRod-&gt;MinRtt,
                pathRod-&gt;MinRtt);
        wprintf(L"\nSum Rtt:             %u", pathRod-&gt;SumRtt);
        wprintf(L"\nCount Rtt:           %u", pathRod-&gt;CountRtt);
        wprintf(L"\nCur Rto:             %u", pathRod-&gt;CurRto);
        wprintf(L"\nMax Rto:             %u", pathRod-&gt;MaxRto);
        wprintf(L"\nMin Rto:             %u", pathRod-&gt;MinRto);
        wprintf(L"\nCur Mss:             %u", pathRod-&gt;CurMss);
        wprintf(L"\nMax Mss:             %u", pathRod-&gt;MaxMss);
        wprintf(L"\nMin Mss:             %u", pathRod-&gt;MinMss);
        wprintf(L"\nSpurious Rto:        %u", pathRod-&gt;SpuriousRtoDetections);
        break;

    case TcpConnectionEstatsSendBuff:
        sndBuffRod = (PTCP_ESTATS_SEND_BUFF_ROD_v0) rod;
        wprintf(L"\n\nSend Buff");
        wprintf(L"\nCur Retx Queue:   %u", sndBuffRod-&gt;CurRetxQueue);
        wprintf(L"\nMax Retx Queue:   %u", sndBuffRod-&gt;MaxRetxQueue);
        wprintf(L"\nCur App W Queue:  %u", sndBuffRod-&gt;CurAppWQueue);
        wprintf(L"\nMax App W Queue:  %u", sndBuffRod-&gt;MaxAppWQueue);
        break;

    case TcpConnectionEstatsRec:
        recRod = (PTCP_ESTATS_REC_ROD_v0) rod;
        wprintf(L"\n\nRec");
        wprintf(L"\nCur Rwin Sent:   0x%x (%u)", recRod-&gt;CurRwinSent,
                recRod-&gt;CurRwinSent);
        wprintf(L"\nMax Rwin Sent:   0x%x (%u)", recRod-&gt;MaxRwinSent,
                recRod-&gt;MaxRwinSent);
        wprintf(L"\nMin Rwin Sent:   0x%x (%u)", recRod-&gt;MinRwinSent,
                recRod-&gt;MinRwinSent);
        wprintf(L"\nLim Rwin:        0x%x (%u)", recRod-&gt;LimRwin,
                recRod-&gt;LimRwin);
        wprintf(L"\nDup Acks:        %u", recRod-&gt;DupAckEpisodes);
        wprintf(L"\nDup Acks Out:    %u", recRod-&gt;DupAcksOut);
        wprintf(L"\nCe Rcvd:         %u", recRod-&gt;CeRcvd);
        wprintf(L"\nEcn Send:        %u", recRod-&gt;EcnSent);
        wprintf(L"\nEcn Nonces Rcvd: %u", recRod-&gt;EcnNoncesRcvd);
        wprintf(L"\nCur Reasm Queue: %u", recRod-&gt;CurReasmQueue);
        wprintf(L"\nMax Reasm Queue: %u", recRod-&gt;MaxReasmQueue);
        wprintf(L"\nCur App R Queue: %u", recRod-&gt;CurAppRQueue);
        wprintf(L"\nMax App R Queue: %u", recRod-&gt;MaxAppRQueue);
        wprintf(L"\nWin Scale Sent:  0x%.2x", recRod-&gt;WinScaleSent);
        break;

    case TcpConnectionEstatsObsRec:
        obsRecRod = (PTCP_ESTATS_OBS_REC_ROD_v0) rod;
        wprintf(L"\n\nObs Rec");
        wprintf(L"\nCur Rwin Rcvd:   0x%x (%u)", obsRecRod-&gt;CurRwinRcvd,
                obsRecRod-&gt;CurRwinRcvd);
        wprintf(L"\nMax Rwin Rcvd:   0x%x (%u)", obsRecRod-&gt;MaxRwinRcvd,
                obsRecRod-&gt;MaxRwinRcvd);
        wprintf(L"\nMin Rwin Rcvd:   0x%x (%u)", obsRecRod-&gt;MinRwinRcvd,
                obsRecRod-&gt;MinRwinRcvd);
        wprintf(L"\nWin Scale Rcvd:  0x%x (%u)", obsRecRod-&gt;WinScaleRcvd,
                obsRecRod-&gt;WinScaleRcvd);
        break;

    case TcpConnectionEstatsBandwidth:
        bandwidthRod = (PTCP_ESTATS_BANDWIDTH_ROD_v0) rod;
        wprintf(L"\n\nBandwidth");
        wprintf(L"\nOutbound Bandwidth:   %lu",
                bandwidthRod-&gt;OutboundBandwidth);
        wprintf(L"\nInbound Bandwidth:    %lu", bandwidthRod-&gt;InboundBandwidth);
        wprintf(L"\nOutbound Instability: %lu",
                bandwidthRod-&gt;OutboundInstability);
        wprintf(L"\nInbound Instability:  %lu",
                bandwidthRod-&gt;InboundInstability);
        wprintf(L"\nOutbound Bandwidth Peaked: %s",
                bandwidthRod-&gt;OutboundBandwidthPeaked ? L"Yes" : L"No");
        wprintf(L"\nInbound Bandwidth Peaked:  %s",
                bandwidthRod-&gt;InboundBandwidthPeaked ? L"Yes" : L"No");
        break;

    case TcpConnectionEstatsFineRtt:
        fineRttRod = (PTCP_ESTATS_FINE_RTT_ROD_v0) rod;
        wprintf(L"\n\nFine RTT");
        wprintf(L"\nRtt Var: %u", fineRttRod-&gt;RttVar);
        wprintf(L"\nMax Rtt: %u", fineRttRod-&gt;MaxRtt);
        wprintf(L"\nMin Rtt: 0x%x (%u) ", fineRttRod-&gt;MinRtt,
                fineRttRod-&gt;MinRtt);
        wprintf(L"\nSum Rtt: %u", fineRttRod-&gt;SumRtt);
        break;

    default:
        wprintf(L"\nCannot get type %d", type);
        break;
    }
    }
        
    free(ros);
    free(rod);
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/77150609-d06d-4492-bbd7-21eecd825bde">GetTcp6Table</a>



<a href="https://msdn.microsoft.com/b3e9eda5-5e86-4790-8b1b-ca9bae44b502">MIB_TCP6ROW</a>



<a href="https://msdn.microsoft.com/62bb8544-0a0a-40b5-92cf-9631c9a9987c">MIB_TCP6TABLE</a>



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



<a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a>



<a href="https://msdn.microsoft.com/dd179e9b-86e6-48e8-bb4b-05d69b9794b2">TCP_SOFT_ERROR</a>
 

 

