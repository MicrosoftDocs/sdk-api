---
UID: NS:tcpmib._MIB_TCP6TABLE
title: MIB_TCP6TABLE (tcpmib.h)
description: Contains a table of TCP connections for IPv6 on the local computer.
helpviewer_keywords: ["*PMIB_TCP6TABLE","MIB_TCP6TABLE","MIB_TCP6TABLE structure [MIB]","PMIB_TCP6TABLE","PMIB_TCP6TABLE structure pointer [MIB]","mib.mib_tcp6table","tcpmib/MIB_TCP6TABLE","tcpmib/PMIB_TCP6TABLE"]
old-location: mib\mib_tcp6table.htm
tech.root: MIB
ms.assetid: 62bb8544-0a0a-40b5-92cf-9631c9a9987c
ms.date: 12/05/2018
ms.keywords: '*PMIB_TCP6TABLE, MIB_TCP6TABLE, MIB_TCP6TABLE structure [MIB], PMIB_TCP6TABLE, PMIB_TCP6TABLE structure pointer [MIB], mib.mib_tcp6table, tcpmib/MIB_TCP6TABLE, tcpmib/PMIB_TCP6TABLE'
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
req.typenames: MIB_TCP6TABLE, *PMIB_TCP6TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_TCP6TABLE
 - tcpmib/_MIB_TCP6TABLE
 - PMIB_TCP6TABLE
 - tcpmib/PMIB_TCP6TABLE
 - MIB_TCP6TABLE
 - tcpmib/MIB_TCP6TABLE
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
 - MIB_TCP6TABLE
---

# MIB_TCP6TABLE structure


## -description

The 
<b>MIB_TCP6TABLE</b> structure contains a table of TCP connections for IPv6 on the local computer.

## -struct-fields

### -field dwNumEntries

A value that specifies the number of TCP connections in the array.

### -field table

An array of 
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a> structures containing TCP connection entries.

## -remarks

The <b>MIB_TCP6TABLE</b> structure is defined on Windows Vista and later. 

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a> function retrieves the IPv6 TCP connection table on the local computer and returns this information in a <b>MIB_TCP6TABLE</b> structure. 

An array of <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a> structures are contained in the <b>MIB_TCP6TABLE</b> structure. 

The <b>MIB_TCP6TABLE</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_TCP6ROW</b> array entries in the <b>table</b> member. Any access to a <b>MIB_TCP6ROW</b> array entry should assume  padding may exist. 




#### Examples

The following example retrieves the TCP connection table for IPv6 as a <b>MIB_TCP6TABLE</b> structure and prints the state of each connection represented as a <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a> structure.


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



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table2">GetTcp6Table2</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcptable">GetTcpTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcptable2">GetTcpTable2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row2">MIB_TCP6ROW2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table2">MIB_TCP6TABLE2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_lh">MIB_TCPROW</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow2">MIB_TCPROW2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable2">MIB_TCPTABLE2</a>