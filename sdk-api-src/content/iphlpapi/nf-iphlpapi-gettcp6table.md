---
UID: NF:iphlpapi.GetTcp6Table
title: GetTcp6Table function (iphlpapi.h)
description: Retrieves the TCP connection table for IPv6. (GetTcp6Table)
helpviewer_keywords: ["GetTcp6Table","GetTcp6Table function [IP Helper]","iphlp.gettcp6table","iphlpapi/GetTcp6Table"]
old-location: iphlp\gettcp6table.htm
tech.root: IpHlp
ms.assetid: 77150609-d06d-4492-bbd7-21eecd825bde
ms.date: 12/05/2018
ms.keywords: GetTcp6Table, GetTcp6Table function [IP Helper], iphlp.gettcp6table, iphlpapi/GetTcp6Table
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
 - GetTcp6Table
 - iphlpapi/GetTcp6Table
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
 - GetTcp6Table
---

# GetTcp6Table function


## -description

The 
<b>GetTcp6Table</b> function retrieves the TCP connection table for IPv6.

## -parameters

### -param TcpTable [out]

A pointer to a buffer that receives the TCP connection table for IPv6 as a 
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table">MIB_TCP6TABLE</a> structure.

### -param SizePointer [in, out]

On input, specifies the size in bytes of the buffer pointed to by the <i>TcpTable</i> parameter.

On output, if the buffer is not large enough to hold the returned TCP connection table, the function sets this parameter equal to the required buffer size in bytes.

### -param Order [in]

A Boolean value that specifies whether the TCP connection table should be sorted. If this parameter is <b>TRUE</b>, the table is sorted in ascending order, starting with the lowest local IP address.  If this parameter is <b>FALSE</b>, the table appears in the order in which they were retrieved.

The following values are compared (as listed) when ordering the TCP endpoints:


<ol>
<li>Local IPv6 address</li>
<li>Local scope ID</li>
<li>Local port</li>
<li>Remote IPv6 address</li>
<li>Remote scope ID</li>
<li>Remote port</li>
</ol>

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
The buffer pointed to by the <i>TcpTable</i> parameter is not large enough. The required size is returned in the variable pointed to by the <i>SizePointer</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>SizePointer</i> parameter is <b>NULL</b>, or 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a> is unable to write to the memory pointed to by the <i>SizePointer</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function is not supported on the operating system in use on the local system.

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

The <b>GetTcp6Table</b> function is defined on Windows Vista and later. 


#### Examples

The following example retrieves the TCP connection table for IPv6 and prints the state of each connection.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

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

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry">GetOwnerModuleFromTcp6Entry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table2">GetTcp6Table2</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatisticsex">GetTcpStatisticsEx</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcptable2">GetTcpTable2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row_owner_module">MIB_TCP6ROW_OWNER_MODULE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row_owner_pid">MIB_TCP6ROW_OWNER_PID</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table">MIB_TCP6TABLE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_module">MIB_TCP6TABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_pid">MIB_TCP6TABLE_OWNER_PID</a>
