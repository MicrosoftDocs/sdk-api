---
UID: NS:tcpmib._MIB_TCPROW_LH
title: "_MIB_TCPROW_LH"
author: windows-sdk-content
description: Contains information that descibes an IPv4 TCP connection.
old-location: mib\mib_tcprow.htm
old-project: mib
ms.assetid: 36364854-caa8-4652-be8e-f741b36d9fd7
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: "*PMIB_TCPROW, *PMIB_TCPROW_LH, MIB_TCPROW, MIB_TCPROW structure [MIB], MIB_TCPROW_LH, MIB_TCPROW_W2K, MIB_TCP_STATE_CLOSED, MIB_TCP_STATE_CLOSE_WAIT, MIB_TCP_STATE_CLOSING, MIB_TCP_STATE_DELETE_TCB, MIB_TCP_STATE_ESTAB, MIB_TCP_STATE_FIN_WAIT1, MIB_TCP_STATE_FIN_WAIT2, MIB_TCP_STATE_LAST_ACK, MIB_TCP_STATE_LISTEN, MIB_TCP_STATE_SYN_RCVD, MIB_TCP_STATE_SYN_SENT, MIB_TCP_STATE_TIME_WAIT, PMIB_TCPROW, PMIB_TCPROW structure pointer [MIB], _MIB_TCPROW_LH, _mpr_mib_tcprow, iprtrmib/MIB_TCPROW, iprtrmib/PMIB_TCPROW, mib.mib_tcprow, rras.mib_tcprow, tcpmib/MIB_TCPROW, tcpmib/PMIB_TCPROW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tcpmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MIB_TCPROW_LH, *PMIB_TCPROW_LH
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpmib.h
 - Iprtrmib.h
api_name:
 - MIB_TCPROW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _MIB_TCPROW_LH structure


## -description


The 
<b>MIB_TCPROW</b> structure contains information that descibes an IPv4 TCP connection.


## -struct-fields




### -field dwState

Type: <b>DWORD</b>

The state of the TCP connection. This member can be one of the values defined in the <i>Iprtrmib.h</i> header file.
					

On the Windows SDK released for Windows Vista
   and later, the organization of header files has changed. This member can be one of the values from the <b>MIB_TCP_STATE</b> enumeration defined in the <i>Tcpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

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
 


### -field State

 


### -field dwLocalAddr

Type: <b>DWORD</b>

The local IPv4 address for the TCP connection on the local computer. A value of zero indicates the listener  can accept a connection on any interface.


### -field dwLocalPort

Type: <b>DWORD</b>

The local port number in network byte order for the TCP connection on the local computer.

 The maximum size of an IP port number is 16 bits, so only the lower 16 bits should be used. The upper 16 bits may contain uninitialized data. 


### -field dwRemoteAddr

Type: <b>DWORD</b>

The IPv4 address for the TCP connection on the remote computer. When the <b>dwState</b> member is <b>MIB_TCP_STATE_LISTEN</b>, this value has no meaning.


### -field dwRemotePort

Type: <b>DWORD</b>

The remote port number in network byte order for the TCP connection on the remote computer. When the <b>dwState</b> member is <b>MIB_TCP_STATE_LISTEN</b>, this member has no meaning. 

The maximum size of an IP port number is 16 bits, so only the lower 16 bits should be used. The upper 16 bits may contain uninitialized data.


## -remarks



The <a href="https://msdn.microsoft.com/e90c5aa0-3126-489b-af44-bf86cb45a6d1">GetTcpTable</a>
			function retrieves the IPv4 TCP connection table on the local computer and returns this information in a <a href="https://msdn.microsoft.com/a8ed8ac2-a72f-4099-ac99-a8b0b77b7b84">MIB_TCPTABLE</a> structure. 

An array of <b>MIB_TCPROW</b> structures are contained in the <b>MIB_TCPTABLE</b> structure. The <b>MIB_TCPROW</b> structure is also used by the <a href="_iphlp_settcpentry">SetTcpEntry</a> function.

  The <b>dwState</b> member indicates the state of the TCP entry in a TCP state diagram. A TCP connection progresses through a series of states during its
  lifetime.  The states are:  LISTEN, SYN-SENT, SYN-RECEIVED,
  ESTABLISHED, FIN-WAIT-1, FIN-WAIT-2, CLOSE-WAIT, CLOSING, LAST-ACK,
  TIME-WAIT, and the fictional state CLOSED.  The CLOSED state is fictional
  because it represents the state when there is no Transmission Control Block, and therefore,
  no connection.  The TCP protocol is described in RFC 793. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84069">http://www.ietf.org/rfc/rfc793.txt</a>. 

The <b>dwLocalAddr</b> and <b>dwRemoteAddr</b> members are stored as a <b>DWORD</b> in the same format as the  <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a> structure. In order to use the <b>dwLocalAddr</b> or <b>dwRemoteAddr</b> members, the <a href="https://msdn.microsoft.com/04673bef-22c6-424f-a5ae-689fb648b54e">ntohl</a> or <a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. On Windows Vista
   and later, the <a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a> or <a href="https://msdn.microsoft.com/4244eaaf-8522-4edb-abb8-dc2b063c9076">RtlIpv4AddressToStringEx</a> functions may be used to convert the IPv4 address in the <b>dwLocalAddr</b> or <b>dwRemoteAddr</b> members to a string without loading the Windows Sockets DLL. 

The <b>dwLocalPort</b>, and <b>dwRemotePort</b> members are in network byte order. In order to use the <b>dwLocalPort</b> or <b>dwRemotePort</b> members, the <a href="https://msdn.microsoft.com/9946df13-3b40-4bcb-91ca-10684b3fc9a5">ntohs</a> or <a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <b>MIB_TCPROW</b> structure changed slightly on Windows Vista and later. On Windows Vista
   and later, the <b>dwState</b> member is replaced by  a union that contains the following members.



<table>
<tr>
<th>Member</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="DWORD_dwState"></a><a id="dword_dwstate"></a><a id="DWORD_DWSTATE"></a>DWORD dwState

</td>
<td width="60%">
The state of the TCP connection.

</td>
</tr>
<tr>
<td width="40%">
<a id="MIB_TCP_STATE_State"></a><a id="mib_tcp_state_state"></a><a id="MIB_TCP_STATE_STATE"></a>MIB_TCP_STATE State

</td>
<td width="60%">
The state of the TCP connection. This member can be one of the values from the <b>MIB_TCP_STATE</b> enumeration type defined in the <i>Tcpmib.h</i> header file. The possible values are the same as those defined for the <b>dwState</b> member. 

</td>
</tr>
</table>
 

In the Windows SDK, the version of the structure for use on Windows Vista and later is  defined as <b>MIB_TCPROW_LH</b>. In the Windows SDK, the version of this structure to be used on earlier systems including Windows 2000 and later is defined as <b>MIB_TCPROW_W2K</b>. When compiling an application if the target platform is Windows Vista and later (<code>NTDDI_VERSION &gt;= NTDDI_LONGHORN</code>, <code>_WIN32_WINNT &gt;= 0x0600</code>, or <code>WINVER &gt;= 0x0600</code>), the <b>MIB_TCPROW_LH</b> structure is typedefed to the <b>MIB_TCPROW</b> structure. When compiling an application if the target platform is not Windows Vista and later, the <b>MIB_TCPROW_W2K</b> structure is typedefed to the <b>MIB_TCPROW</b> structure. 

On the Windows SDK released for Windows Vista
   and later, the organization of header files has changed. This  structure is defined in the <i>Tcpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.


#### Examples

The following example retrieves the TCP connection table and prints the state of each connection represented as a <b>MIB_TCPROW</b> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;

// Need to link with Iphlpapi.lib and Ws2_32.lib
#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

/* Note: could also use malloc() and free() */

int main()
{

    // Declare and initialize variables
    PMIB_TCPTABLE pTcpTable;
    DWORD dwSize = 0;
    DWORD dwRetVal = 0;

    char szLocalAddr[128];
    char szRemoteAddr[128];

    struct in_addr IpAddr;

    int i;

    pTcpTable = (MIB_TCPTABLE *) MALLOC(sizeof (MIB_TCPTABLE));
    if (pTcpTable == NULL) {
        printf("Error allocating memory\n");
        return 1;
    }

    dwSize = sizeof (MIB_TCPTABLE);
// Make an initial call to GetTcpTable to
// get the necessary size into the dwSize variable
    if ((dwRetVal = GetTcpTable(pTcpTable, &amp;dwSize, TRUE)) ==
        ERROR_INSUFFICIENT_BUFFER) {
        FREE(pTcpTable);
        pTcpTable = (MIB_TCPTABLE *) MALLOC(dwSize);
        if (pTcpTable == NULL) {
            printf("Error allocating memory\n");
            return 1;
        }
    }
// Make a second call to GetTcpTable to get
// the actual data we require
    if ((dwRetVal = GetTcpTable(pTcpTable, &amp;dwSize, TRUE)) == NO_ERROR) {
        printf("\tNumber of entries: %d\n", (int) pTcpTable-&gt;dwNumEntries);
        for (i = 0; i &lt; (int) pTcpTable-&gt;dwNumEntries; i++) {
            printf("\n\tTCP[%d] State: %ld - ", i,
                   pTcpTable-&gt;table[i].dwState);
            switch (pTcpTable-&gt;table[i].dwState) {
            case MIB_TCP_STATE_CLOSED:
                printf("CLOSED\n");
                break;
            case MIB_TCP_STATE_LISTEN:
                printf("LISTEN\n");
                break;
            case MIB_TCP_STATE_SYN_SENT:
                printf("SYN-SENT\n");
                break;
            case MIB_TCP_STATE_SYN_RCVD:
                printf("SYN-RECEIVED\n");
                break;
            case MIB_TCP_STATE_ESTAB:
                printf("ESTABLISHED\n");
                break;
            case MIB_TCP_STATE_FIN_WAIT1:
                printf("FIN-WAIT-1\n");
                break;
            case MIB_TCP_STATE_FIN_WAIT2:
                printf("FIN-WAIT-2 \n");
                break;
            case MIB_TCP_STATE_CLOSE_WAIT:
                printf("CLOSE-WAIT\n");
                break;
            case MIB_TCP_STATE_CLOSING:
                printf("CLOSING\n");
                break;
            case MIB_TCP_STATE_LAST_ACK:
                printf("LAST-ACK\n");
                break;
            case MIB_TCP_STATE_TIME_WAIT:
                printf("TIME-WAIT\n");
                break;
            case MIB_TCP_STATE_DELETE_TCB:
                printf("DELETE-TCB\n");
                break;
            default:
                printf("UNKNOWN dwState value: %d\n", pTcpTable-&gt;table[i].dwState);
                break;
            }

            IpAddr.S_un.S_addr = (u_long) pTcpTable-&gt;table[i].dwLocalAddr;
            strcpy_s(szLocalAddr, sizeof (szLocalAddr), inet_ntoa(IpAddr));
            printf("\tTCP[%d] Local Addr: %s\n", i, szLocalAddr);

            printf("\tTCP[%d] Local Port: %d \n", i,
                   ntohs((u_short)pTcpTable-&gt;table[i].dwLocalPort));

            IpAddr.S_un.S_addr = (u_long) pTcpTable-&gt;table[i].dwRemoteAddr;
            strcpy_s(szRemoteAddr, sizeof (szRemoteAddr), inet_ntoa(IpAddr));
            printf("\tTCP[%d] Remote Addr: %s\n", i, szRemoteAddr);

            printf("\tTCP[%d] Remote Port: %d\n", i,
                   ntohs((u_short)pTcpTable-&gt;table[i].dwRemotePort));
        }
    } else {
        printf("\tGetTcpTable failed with %d\n", dwRetVal);
        FREE(pTcpTable);
        return 1;
    }

    if (pTcpTable != NULL) {
        FREE(pTcpTable);
        pTcpTable = NULL;
    }    

    return 0;    
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/77150609-d06d-4492-bbd7-21eecd825bde">GetTcp6Table</a>



<a href="https://msdn.microsoft.com/435b9198-b921-407c-9441-31cfe77c03f1">GetTcp6Table2</a>



<a href="https://msdn.microsoft.com/e90c5aa0-3126-489b-af44-bf86cb45a6d1">GetTcpTable</a>



<a href="https://msdn.microsoft.com/942e8cb6-545f-45ab-919a-246e3b2d4c6a">GetTcpTable2</a>



<a href="https://msdn.microsoft.com/b3e9eda5-5e86-4790-8b1b-ca9bae44b502">MIB_TCP6ROW</a>



<b>MIB_TCP6ROW2</b>



<a href="https://msdn.microsoft.com/62bb8544-0a0a-40b5-92cf-9631c9a9987c">MIB_TCP6TABLE</a>



<a href="https://msdn.microsoft.com/3cb8568e-ce31-4ed1-aa9e-abcb826c0cea">MIB_TCP6TABLE2</a>



<a href="https://msdn.microsoft.com/cff343cd-fe85-4e60-87bd-c1e9833cea38">MIB_TCPROW2</a>



<a href="https://msdn.microsoft.com/a8ed8ac2-a72f-4099-ac99-a8b0b77b7b84">MIB_TCPTABLE</a>



<a href="https://msdn.microsoft.com/e07de994-0bd5-4d18-9012-8ff191dd6939">MIB_TCPTABLE2</a>



<a href="https://msdn.microsoft.com/f198b770-9429-4b51-9fb4-06cf9917bc21">RtlIpv4AddressToString</a>



<a href="https://msdn.microsoft.com/4244eaaf-8522-4edb-abb8-dc2b063c9076">RtlIpv4AddressToStringEx</a>



<a href="_iphlp_settcpentry">SetTcpEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>



<a href="https://msdn.microsoft.com/04673bef-22c6-424f-a5ae-689fb648b54e">ntohl</a>



<a href="https://msdn.microsoft.com/9946df13-3b40-4bcb-91ca-10684b3fc9a5">ntohs</a>
 

 

