---
UID: NF:iphlpapi.GetTcpTable
title: GetTcpTable function
author: windows-sdk-content
description: Retrieves the IPv4 TCP connection table.
old-location: iphlp\gettcptable.htm
old-project: iphlp
ms.assetid: e90c5aa0-3126-489b-af44-bf86cb45a6d1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTcpTable, GetTcpTable function [IP Helper], _iphlp_gettcptable, iphlp.gettcptable, iphlpapi/GetTcpTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - GetTcpTable
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetTcpTable function


## -description


The 
<b>GetTcpTable</b> function retrieves the IPv4 TCP connection table.


## -parameters




### -param TcpTable [out]

A pointer to a buffer that receives the TCP connection table as a 
<a href="https://msdn.microsoft.com/a8ed8ac2-a72f-4099-ac99-a8b0b77b7b84">MIB_TCPTABLE</a> structure.


### -param SizePointer [in, out]

On input, specifies the size in  bytes  of the buffer pointed to by the <i>pTcpTable</i> parameter.

On output, if the buffer is not large enough to hold the returned connection table, the function sets this parameter equal to the required buffer size in bytes.

On the Windows SDK released for Windows Vista and later, the data type for this parameter is changed to a <b>PULONG</b> which is equivalent to a <b>PDWORD</b>. 


### -param Order [in]

A Boolean value that specifies whether the TCP connection table should be sorted. If this parameter is <b>TRUE</b>, the table is sorted in the order of: 


<ol>
<li>Local IP address</li>
<li>Local port</li>
<li>Remote IP address</li>
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
The buffer pointed to by the <i>pTcpTable</i> parameter is not large enough. The required size is returned in the <b>DWORD</b> variable pointed to by the <i>pdwSize</i> parameter.

This error is also returned if the <i>pTcpTable</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwSize</i> parameter is <b>NULL</b>, or 
<a href="https://msdn.microsoft.com/e90c5aa0-3126-489b-af44-bf86cb45a6d1">GetTcpTable</a> is unable to write to the memory pointed to by the <i>pdwSize</i> parameter.

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
<dt><b>STATUS_UNSUCCESSFUL</b></dt>
</dl>
</td>
<td width="60%">
If you receive this return code then calling the function again is usually enough to clear the issue and get the desired result. This return code can be a consequence of the system being under high load. For example, if the size of the TCP connection table changes by more than 2 additional items 3 consecutive times.

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



On the Windows SDK released for Windows Vista and later, the return value from the <b>GetTcpTable</b> function is changed to a data type of <b>ULONG</b> which is equivalent to a <b>DWORD</b>. 


#### Examples

The following example retrieves the TCP connection table for IPv4 and prints the state of each connection.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Need to link with Iphlpapi.lib and Ws2_32.lib
#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;

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
            IpAddr.S_un.S_addr = (u_long) pTcpTable-&gt;table[i].dwLocalAddr;
            strcpy_s(szLocalAddr, sizeof (szLocalAddr), inet_ntoa(IpAddr));
            IpAddr.S_un.S_addr = (u_long) pTcpTable-&gt;table[i].dwRemoteAddr;
            strcpy_s(szRemoteAddr, sizeof (szRemoteAddr), inet_ntoa(IpAddr));

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
                printf("UNKNOWN dwState value\n");
                break;
            }
            printf("\tTCP[%d] Local Addr: %s\n", i, szLocalAddr);
            printf("\tTCP[%d] Local Port: %d \n", i,
                   ntohs((u_short)pTcpTable-&gt;table[i].dwLocalPort));
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




<a href="https://msdn.microsoft.com/96356a0e-ae0d-4000-9223-a578cbdeaa8b">GetExtendedTcpTable</a>



<a href="https://msdn.microsoft.com/12162f0a-56c1-4f81-a1f5-3cd5ad975d0d">GetOwnerModuleFromTcpEntry</a>



<a href="https://msdn.microsoft.com/77150609-d06d-4492-bbd7-21eecd825bde">GetTcp6Table</a>



<a href="https://msdn.microsoft.com/435b9198-b921-407c-9441-31cfe77c03f1">GetTcp6Table2</a>



<a href="https://msdn.microsoft.com/841cdeaa-6284-4b39-a218-69937eca1982">GetTcpStatistics</a>



<a href="https://msdn.microsoft.com/78cfc69d-eae8-49c1-a460-6527a61f773d">GetTcpStatisticsEx</a>



<a href="https://msdn.microsoft.com/942e8cb6-545f-45ab-919a-246e3b2d4c6a">GetTcpTable2</a>



<a href="https://msdn.microsoft.com/36364854-caa8-4652-be8e-f741b36d9fd7">MIB_TCPROW</a>



<a href="https://msdn.microsoft.com/5fc1e95a-4ab1-4a15-aedc-47cfd811c035">MIB_TCPROW_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/220b69a4-b372-4eff-8d5a-eca0d39b8af9">MIB_TCPROW_OWNER_PID</a>



<a href="https://msdn.microsoft.com/a8ed8ac2-a72f-4099-ac99-a8b0b77b7b84">MIB_TCPTABLE</a>



<a href="https://msdn.microsoft.com/d44c9d82-906b-43ea-8edd-cf973864668d">MIB_TCPTABLE_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/ef39b832-1f22-468a-8734-c7d9bd3ac965">MIB_TCPTABLE_OWNER_PID</a>



<a href="https://msdn.microsoft.com/5916f66d-3c85-406d-b6f9-6c1c84161be4">SetTcpEntry</a>
 

 

