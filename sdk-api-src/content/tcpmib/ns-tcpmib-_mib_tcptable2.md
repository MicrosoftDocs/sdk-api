---
UID: NS:tcpmib._MIB_TCPTABLE2
title: "_MIB_TCPTABLE2"
author: windows-sdk-content
description: Contains a table of IPv4 TCP connections on the local computer.
old-location: mib\mib_tcptable2.htm
old-project: mib
ms.assetid: e07de994-0bd5-4d18-9012-8ff191dd6939
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PMIB_TCPTABLE2, MIB_TCPTABLE2, MIB_TCPTABLE2 structure [MIB], PMIB_TCPTABLE2, PMIB_TCPTABLE2 structure pointer [MIB], _MIB_TCPTABLE2, mib.mib_tcptable2, tcpmib/MIB_TCPTABLE2, tcpmib/PMIB_TCPTABLE2"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tcpmib.h
req.include-header: Iphlpapi.h
req.redist: 
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
req.typenames: MIB_TCPTABLE2, *PMIB_TCPTABLE2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpmib.h
api_name:
 - MIB_TCPTABLE2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _MIB_TCPTABLE2 structure


## -description


The 
<b>MIB_TCPTABLE2</b> structure contains a table of IPv4 TCP connections on the local computer.


## -struct-fields




### -field dwNumEntries

The number of entries in the table.


### -field table

A pointer to a table of TCP connections implemented as an array of 
<a href="https://msdn.microsoft.com/cff343cd-fe85-4e60-87bd-c1e9833cea38">MIB_TCPROW2</a> structures.


## -remarks



The <a href="https://msdn.microsoft.com/942e8cb6-545f-45ab-919a-246e3b2d4c6a">GetTcpTable2</a>function retrieves the IPv4 TCP connection table on the local computer and returns this information in a <b>MIB_TCPTABLE2</b> structure. An array of <a href="https://msdn.microsoft.com/cff343cd-fe85-4e60-87bd-c1e9833cea38">MIB_TCPROW2</a> structures are contained in the <b>MIB_TCPTABLE2</b> structure. 



The <b>MIB_TCPTABLE2</b> structure may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="https://msdn.microsoft.com/cff343cd-fe85-4e60-87bd-c1e9833cea38">MIB_TCPROW2</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_TCPROW2</b> array entries in the <b>table</b> member. Any access to a <b>MIB_TCPROW2</b> array entry should assume  padding may exist. 




#### Examples

The following example retrieves the TCP connection table for IPv4 as a <b>MIB_TCPTABLE2</b> structure prints the state of each connection represented as a <a href="https://msdn.microsoft.com/cff343cd-fe85-4e60-87bd-c1e9833cea38">MIB_TCPROW2</a> structure.

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
    PMIB_TCPTABLE2 pTcpTable;
    ULONG ulSize = 0;
    DWORD dwRetVal = 0;

    char szLocalAddr[128];
    char szRemoteAddr[128];

    struct in_addr IpAddr;

    int i;

    pTcpTable = (MIB_TCPTABLE2 *) MALLOC(sizeof (MIB_TCPTABLE2));
    if (pTcpTable == NULL) {
        printf("Error allocating memory\n");
        return 1;
    }

    ulSize = sizeof (MIB_TCPTABLE);
// Make an initial call to GetTcpTable2 to
// get the necessary size into the ulSize variable
    if ((dwRetVal = GetTcpTable2(pTcpTable, &amp;ulSize, TRUE)) ==
        ERROR_INSUFFICIENT_BUFFER) {
        FREE(pTcpTable);
        pTcpTable = (MIB_TCPTABLE2 *) MALLOC(ulSize);
        if (pTcpTable == NULL) {
            printf("Error allocating memory\n");
            return 1;
        }
    }
// Make a second call to GetTcpTable2 to get
// the actual data we require
    if ((dwRetVal = GetTcpTable2(pTcpTable, &amp;ulSize, TRUE)) == NO_ERROR) {
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
                wprintf(L"UNKNOWN dwState value: %d\n", pTcpTable-&gt;table[i].dwState);
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
                   
            printf("\tTCP[%d] Owning PID: %d\n", i, pTcpTable-&gt;table[i].dwOwningPid);

            printf("\tTCP[%d] Offload State: %ld - ", i,
                   pTcpTable-&gt;table[i].dwOffloadState);
            switch (pTcpTable-&gt;table[i].dwOffloadState) {
            case TcpConnectionOffloadStateInHost:
                printf("Owned by the network stack and not offloaded \n");
                break;
            case TcpConnectionOffloadStateOffloading:
                printf("In the process of being offloaded\n");
                break;
            case TcpConnectionOffloadStateOffloaded:
                printf("Offloaded to the network interface control\n");
                break;
            case TcpConnectionOffloadStateUploading:
                printf("In the process of being uploaded back to the network stack \n");
                break;
            default:
                printf("UNKNOWN Offload state value\n");
                break;
            }
                   
        }
    } else {
        printf("\tGetTcpTable2 failed with %d\n", dwRetVal);
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



<a href="https://msdn.microsoft.com/bbec3397-0317-40f7-926f-2ec48cf5386d">MIB_TCP6ROW2</a>



<a href="https://msdn.microsoft.com/62bb8544-0a0a-40b5-92cf-9631c9a9987c">MIB_TCP6TABLE</a>



<a href="https://msdn.microsoft.com/3cb8568e-ce31-4ed1-aa9e-abcb826c0cea">MIB_TCP6TABLE2</a>



<a href="https://msdn.microsoft.com/36364854-caa8-4652-be8e-f741b36d9fd7">MIB_TCPROW</a>



<a href="https://msdn.microsoft.com/cff343cd-fe85-4e60-87bd-c1e9833cea38">MIB_TCPROW2</a>



<a href="https://msdn.microsoft.com/a8ed8ac2-a72f-4099-ac99-a8b0b77b7b84">MIB_TCPTABLE</a>
 

 

