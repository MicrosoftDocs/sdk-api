---
UID: NS:tcpmib._MIB_TCP6ROW
title: MIB_TCP6ROW (tcpmib.h)
description: Contains information that describes an IPv6 TCP connection. (MIB_TCP6ROW)
helpviewer_keywords: ["*PMIB_TCP6ROW","MIB_TCP6ROW","MIB_TCP6ROW structure [MIB]","MIB_TCP_STATE_CLOSED","MIB_TCP_STATE_CLOSE_WAIT","MIB_TCP_STATE_CLOSING","MIB_TCP_STATE_DELETE_TCB","MIB_TCP_STATE_ESTAB","MIB_TCP_STATE_FIN_WAIT1","MIB_TCP_STATE_FIN_WAIT2","MIB_TCP_STATE_LAST_ACK","MIB_TCP_STATE_LISTEN","MIB_TCP_STATE_SYN_RCVD","MIB_TCP_STATE_SYN_SENT","MIB_TCP_STATE_TIME_WAIT","PMIB_TCP6ROW","PMIB_TCP6ROW structure pointer [MIB]","mib.mib_tcp6row","tcpmib/MIB_TCP6ROW","tcpmib/PMIB_TCP6ROW"]
old-location: mib\mib_tcp6row.htm
tech.root: MIB
ms.assetid: b3e9eda5-5e86-4790-8b1b-ca9bae44b502
ms.date: 12/05/2018
ms.keywords: '*PMIB_TCP6ROW, MIB_TCP6ROW, MIB_TCP6ROW structure [MIB], MIB_TCP_STATE_CLOSED, MIB_TCP_STATE_CLOSE_WAIT, MIB_TCP_STATE_CLOSING, MIB_TCP_STATE_DELETE_TCB, MIB_TCP_STATE_ESTAB, MIB_TCP_STATE_FIN_WAIT1, MIB_TCP_STATE_FIN_WAIT2, MIB_TCP_STATE_LAST_ACK, MIB_TCP_STATE_LISTEN, MIB_TCP_STATE_SYN_RCVD, MIB_TCP_STATE_SYN_SENT, MIB_TCP_STATE_TIME_WAIT, PMIB_TCP6ROW, PMIB_TCP6ROW structure pointer [MIB], mib.mib_tcp6row, tcpmib/MIB_TCP6ROW, tcpmib/PMIB_TCP6ROW'
req.header: tcpmib.h
req.include-header: Iphlpapi.h
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
req.typenames: MIB_TCP6ROW, *PMIB_TCP6ROW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_TCP6ROW
 - tcpmib/_MIB_TCP6ROW
 - PMIB_TCP6ROW
 - tcpmib/PMIB_TCP6ROW
 - MIB_TCP6ROW
 - tcpmib/MIB_TCP6ROW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpmib.h
api_name:
 - MIB_TCP6ROW
---

# MIB_TCP6ROW structure


## -description

The 
<b>MIB_TCP6ROW</b> structure contains information that describes an IPv6  TCP connection.

## -struct-fields

### -field State

Type: <b>MIB_TCP_STATE</b>

The state of the TCP connection. This member can be one of the values from the <b>MIB_TCP_STATE</b> enumeration type defined in the <i>Tcpmib.h</i> header file. 
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_CLOSED"></a><a id="mib_tcp_state_closed"></a><dl>
<dt><b>MIB_TCP_STATE_CLOSED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the CLOSED state that represents no connection state at all.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_LISTEN"></a><a id="mib_tcp_state_listen"></a><dl>
<dt><b>MIB_TCP_STATE_LISTEN</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the LISTEN state waiting for a connection request from any remote
    TCP and port.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_SYN_SENT"></a><a id="mib_tcp_state_syn_sent"></a><dl>
<dt><b>MIB_TCP_STATE_SYN_SENT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the SYN-SENT state waiting for a matching connection request
    after having sent a connection request (SYN packet).

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_SYN_RCVD"></a><a id="mib_tcp_state_syn_rcvd"></a><dl>
<dt><b>MIB_TCP_STATE_SYN_RCVD</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the SYN-RECEIVED state waiting for a confirming connection
    request acknowledgment after having both received and sent a
    connection request (SYN packet).

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_ESTAB"></a><a id="mib_tcp_state_estab"></a><dl>
<dt><b>MIB_TCP_STATE_ESTAB</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the ESTABLISHED state that represents an open connection, data received can be
    delivered to the user.  This is the normal state for the data transfer phase
    of the TCP connection.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_FIN_WAIT1"></a><a id="mib_tcp_state_fin_wait1"></a><dl>
<dt><b>MIB_TCP_STATE_FIN_WAIT1</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The TCP connection is FIN-WAIT-1 state waiting for a connection termination request
    from the remote TCP, or an acknowledgment of the connection
    termination request previously sent.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_FIN_WAIT2"></a><a id="mib_tcp_state_fin_wait2"></a><dl>
<dt><b>MIB_TCP_STATE_FIN_WAIT2</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The TCP connection is FIN-WAIT-1 state waiting for a connection termination request
    from the remote TCP.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_CLOSE_WAIT"></a><a id="mib_tcp_state_close_wait"></a><dl>
<dt><b>MIB_TCP_STATE_CLOSE_WAIT</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the CLOSE-WAIT state waiting for a connection termination request
    from the local user.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_CLOSING"></a><a id="mib_tcp_state_closing"></a><dl>
<dt><b>MIB_TCP_STATE_CLOSING</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the CLOSING state waiting for a connection termination request
    acknowledgment from the remote TCP.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_LAST_ACK"></a><a id="mib_tcp_state_last_ack"></a><dl>
<dt><b>MIB_TCP_STATE_LAST_ACK</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the LAST-ACK state waiting for an acknowledgment of the
    connection termination request previously sent to the remote TCP
    (which includes an acknowledgment of its connection termination
    request). 

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_TIME_WAIT"></a><a id="mib_tcp_state_time_wait"></a><dl>
<dt><b>MIB_TCP_STATE_TIME_WAIT</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the TIME-WAIT state waiting for enough time to pass to be sure
    the remote TCP received the acknowledgment of its connection
    termination request.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_DELETE_TCB"></a><a id="mib_tcp_state_delete_tcb"></a><dl>
<dt><b>MIB_TCP_STATE_DELETE_TCB</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the delete TCB state that represents the deletion of the Transmission Control Block (TCB), a data structure used to maintain information on each TCP entry.

</td>
</tr>
</table>

### -field LocalAddr

Type: <b>IN6_ADDR</b>

The local IPv6 address for the TCP connection on the local computer. A value of zero indicates the listener  can accept a connection on any interface.

### -field dwLocalScopeId

Type: <b>DWORD</b>

The local scope ID for the TCP connection on the local computer.

### -field dwLocalPort

Type: <b>DWORD</b>

The local port number in network byte order for the TCP connection on the local computer.

 The maximum size of an IP port number is 16 bits, so only the lower 16 bits should be used. The upper 16 bits may contain uninitialized data.

### -field RemoteAddr

Type: <b>IN6_ADDR</b>

The IPv6 address for the TCP connection on the remote computer. When the <b>State</b> member is <b>MIB_TCP_STATE_LISTEN</b>, this value has no meaning.

### -field dwRemoteScopeId

Type: <b>DWORD</b>

The remote scope ID for the TCP connection on the remote computer. When the <b>State</b> member is <b>MIB_TCP_STATE_LISTEN</b>, this value has no meaning.

### -field dwRemotePort

Type: <b>DWORD</b>

The remote port number in network byte order for the TCP connection on the remote computer. When the <b>State</b> member is <b>MIB_TCP_STATE_LISTEN</b>, this value has no meaning.

 The maximum size of an IP port number is 16 bits, so only the lower 16 bits should be used. The upper 16 bits may contain uninitialized data.

## -remarks

The <b>MIB_TCP6ROW</b> structure is defined on Windows Vista and later. 

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a> function retrieves the IPv6 TCP connection table on the local computer and returns this information in a <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table">MIB_TCP6TABLE</a> structure. 

An array of <b>MIB_TCP6ROW</b> structures are contained in the <b>MIB_TCP6TABLE</b> structure.  

  The <b>State</b> member indicates the state of the TCP entry in a TCP state diagram. A TCP connection progresses through a series of states during its
  lifetime.  The states are:  LISTEN, SYN-SENT, SYN-RECEIVED,
  ESTABLISHED, FIN-WAIT-1, FIN-WAIT-2, CLOSE-WAIT, CLOSING, LAST-ACK,
  TIME-WAIT, and the fictional state CLOSED.  The CLOSED state is fictional
  because it represents the state when there is no Transmission Control Block, and therefore,
  no connection.  The TCP protocol is described in RFC 793. For more information, see 
<a href="https://www.ietf.org/rfc/rfc793.txt">http://www.ietf.org/rfc/rfc793.txt</a>. 

The <b>dwLocalPort</b>, and <b>dwRemotePort</b> members are in network byte order. In order to use the <b>dwLocalPort</b> or <b>dwRemotePort</b> members, the <a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <b>dwLocalScopeId</b>, and <b>dwRemoteScopeId</b> members are in network byte order. In order to use the <b>dwLocalScopeId</b> or <b>dwRemoteScopeId</b> members, the <a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <b>LocalAddr</b> and <b>RemoteAddr</b> members are stored in  <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in6_addr</a> structures. The <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a> or <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a> functions may be used to convert the IPv6 address in the <b>LocalAddr</b> or <b>RemoteAddr</b> members to a string without loading the Windows Sockets DLL. 


#### Examples

The following example retrieves the TCP connection table for IPv6 and prints the state of each connection represented as a <b>MIB_TCP6ROW</b> structure.


```cpp
#define UNICODE 1

#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

// Need to link with Iphlpapi.lib and Ws2_32.lib
#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))
/* Note: could also use malloc() and free() */

int wmain()
{

    // Declare and initialize variables
    PMIB_TCP6TABLE pTcpTable;
    DWORD dwSize = 0;
    DWORD dwRetVal = 0;

    wchar_t ipstringbuffer[46];
    
    int i;

    pTcpTable = (MIB_TCP6TABLE *) MALLOC(sizeof (MIB_TCP6TABLE));
    if (pTcpTable == NULL) {
        wprintf(L"Error allocating memory\n");
        return 1;
    }

    dwSize = sizeof (MIB_TCP6TABLE);
// Make an initial call to GetTcp6Table to
// get the necessary size into the dwSize variable
    if ((dwRetVal = GetTcp6Table(pTcpTable, &dwSize, TRUE)) ==
        ERROR_INSUFFICIENT_BUFFER) {
        FREE(pTcpTable);
        pTcpTable = (MIB_TCP6TABLE *) MALLOC(dwSize);
        if (pTcpTable == NULL) {
            wprintf(L"Error allocating memory\n");
            return 1;
        }
    }
// Make a second call to GetTcp6Table to get
// the actual data we require
    if ((dwRetVal = GetTcp6Table(pTcpTable, &dwSize, TRUE)) == NO_ERROR) {
        wprintf(L"\tNumber of entries: %d\n", (int) pTcpTable->dwNumEntries);
        for (i = 0; i < (int) pTcpTable->dwNumEntries; i++) {
            wprintf(L"\n\tTCP[%d] State: %ld - ", i,
                   pTcpTable->table[i].State);
            switch (pTcpTable->table[i].State) {
            case MIB_TCP_STATE_CLOSED:
                wprintf(L"CLOSED\n");
                break;
            case MIB_TCP_STATE_LISTEN:
                wprintf(L"LISTEN\n");
                break;
            case MIB_TCP_STATE_SYN_SENT:
                wprintf(L"SYN-SENT\n");
                break;
            case MIB_TCP_STATE_SYN_RCVD:
                wprintf(L"SYN-RECEIVED\n");
                break;
            case MIB_TCP_STATE_ESTAB:
                wprintf(L"ESTABLISHED\n");
                break;
            case MIB_TCP_STATE_FIN_WAIT1:
                wprintf(L"FIN-WAIT-1\n");
                break;
            case MIB_TCP_STATE_FIN_WAIT2:
                wprintf(L"FIN-WAIT-2 \n");
                break;
            case MIB_TCP_STATE_CLOSE_WAIT:
                wprintf(L"CLOSE-WAIT\n");
                break;
            case MIB_TCP_STATE_CLOSING:
                wprintf(L"CLOSING\n");
                break;
            case MIB_TCP_STATE_LAST_ACK:
                wprintf(L"LAST-ACK\n");
                break;
            case MIB_TCP_STATE_TIME_WAIT:
                wprintf(L"TIME-WAIT\n");
                break;
            case MIB_TCP_STATE_DELETE_TCB:
                wprintf(L"DELETE-TCB\n");
                break;
            default:
                wprintf(L"UNKNOWN dwState value\n");
                break;
            }

            if (InetNtop(AF_INET6, &pTcpTable->table[i].LocalAddr, ipstringbuffer, 46) == NULL)
                wprintf(L"  InetNtop function failed for local IPv6 address\n");
            else     
                wprintf(L"\tTCP[%d] Local Addr: %s\n", i, ipstringbuffer);
            wprintf(L"\tTCP[%d] Local Scope ID: %d \n", i,
                   ntohl (pTcpTable->table[i].dwLocalScopeId));
            wprintf(L"\tTCP[%d] Local Port: %d \n", i,
                   ntohs((u_short)pTcpTable->table[i].dwLocalPort));

            if (InetNtop(AF_INET6, &pTcpTable->table[i].RemoteAddr, ipstringbuffer, 46) == NULL)
                wprintf(L"  InetNtop function failed for remote IPv6 address\n");
            else     
                wprintf(L"\tTCP[%d] Remote Addr: %s\n", i, ipstringbuffer);
            wprintf(L"\tTCP[%d] Remote Scope ID: %d \n", i,
                   ntohl(pTcpTable->table[i].dwRemoteScopeId));
            wprintf(L"\tTCP[%d] Remote Port: %d\n", i,
                   ntohs((u_short)pTcpTable->table[i].dwRemotePort));
        }
    } else {
        wprintf(L"\tGetTcp6Table failed with %d\n", dwRetVal);
        FREE(pTcpTable);
        return 1;
    }

    if (pTcpTable != NULL) {
        FREE(pTcpTable);
        pTcpTable = NULL;
    }

    return 0;    
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table">MIB_TCP6TABLE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_lh">MIB_TCPROW</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in6_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a>
