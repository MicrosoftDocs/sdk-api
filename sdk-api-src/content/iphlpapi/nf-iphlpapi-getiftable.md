---
UID: NF:iphlpapi.GetIfTable
title: GetIfTable function
author: windows-sdk-content
description: The GetIfTable function retrieves the MIB-II interface table.
old-location: iphlp\getiftable.htm
tech.root: IpHlp
ms.assetid: 6a46c1df-b274-415e-b842-fc1adf6fa206
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetIfTable, GetIfTable function [IP Helper], _iphlp_getiftable, iphlp.getiftable, iphlpapi/GetIfTable
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetIfTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetIfTable function


## -description


The 
<b>GetIfTable</b> function retrieves the MIB-II interface table.


## -parameters




### -param pIfTable [out]

A pointer to a buffer that receives the interface table as a 
<a href="https://msdn.microsoft.com/7c3ca3d0-b6fe-4e1c-858f-82ffb26622e7">MIB_IFTABLE</a> structure.


### -param pdwSize [in, out]

On input, specifies the size in bytes of the buffer pointed to by the <i>pIfTable</i> parameter.

On output, if the buffer is not large enough to hold the returned interface table, the function sets this parameter equal to the required buffer size in bytes.


### -param bOrder [in]

A Boolean value that specifies whether the returned interface table should be sorted in ascending order by interface index. If this parameter is <b>TRUE</b>, the table is sorted.


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
The buffer pointed to by the <i>pIfTable</i> parameter is not large enough. The required size is returned in the <b>DWORD</b> variable pointed to by the <i>pdwSize</i> parameter.

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
<a href="https://msdn.microsoft.com/6a46c1df-b274-415e-b842-fc1adf6fa206">GetIfTable</a> is unable to write to the memory pointed to by the <i>pdwSize</i> parameter.

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
the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The  
<b>GetIfTable</b> function enumerates physical interfaces on a local system and returns this information in a <a href="https://msdn.microsoft.com/7c3ca3d0-b6fe-4e1c-858f-82ffb26622e7">MIB_IFTABLE</a>structure. The physical interfaces include the software loopback interface. 

The <a href="https://msdn.microsoft.com/0153c41c-b02b-4832-87b3-88dc3a9f4ff1">GetIfTable2</a> and <a href="https://msdn.microsoft.com/d8663894-50b1-4ca2-a1f4-6ca0970795a7">GetIfTable2Ex</a> functions available on Windows Vista and later are an enhanced version of the <b>GetIfTable</b> function that enumerate both the physical and logical interfaces on a local system. Logical interfaces include various WAN Miniport interfaces used for L2TP, PPTP, PPOE, and other tunnel encapsulations.

Interfaces are returned in a <a href="https://msdn.microsoft.com/7c3ca3d0-b6fe-4e1c-858f-82ffb26622e7">MIB_IFTABLE</a> structure in the buffer pointed to by the <i>pIfTable</i> parameter. The <b>MIB_IFTABLE</b> structure contains an interface count and an array of <a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a>structures for each interface. 

Note that the returned <a href="https://msdn.microsoft.com/7c3ca3d0-b6fe-4e1c-858f-82ffb26622e7">MIB_IFTABLE</a> structure pointed to by the <i>pIfTable</i> parameter may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a> array entry in the <b>table</b> member of the <b>MIB_IFTABLE</b> structure. Padding for alignment may also be present between the <b>MIB_IFROW</b> array entries. Any access to a <b>MIB_IFROW</b> array entry should assume  padding may exist. 




#### Examples

The following example retrieves the interface table and prints the number of entries in the table and some data on each entry.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#pragma comment(lib, "IPHLPAPI.lib")

#include &lt;iphlpapi.h&gt;

#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

/* Note: could also use malloc() and free() */

int main()
{

    // Declare and initialize variables.

    DWORD dwSize = 0;
    DWORD dwRetVal = 0;

    unsigned int i, j;

    /* variables used for GetIfTable and GetIfEntry */
    MIB_IFTABLE *pIfTable;
    MIB_IFROW *pIfRow;

    // Allocate memory for our pointers.
    pIfTable = (MIB_IFTABLE *) MALLOC(sizeof (MIB_IFTABLE));
    if (pIfTable == NULL) {
        printf("Error allocating memory needed to call GetIfTable\n");
        return 1;
    }
    // Make an initial call to GetIfTable to get the
    // necessary size into dwSize
    dwSize = sizeof (MIB_IFTABLE);
    if (GetIfTable(pIfTable, &amp;dwSize, FALSE) == ERROR_INSUFFICIENT_BUFFER) {
        FREE(pIfTable);
        pIfTable = (MIB_IFTABLE *) MALLOC(dwSize);
        if (pIfTable == NULL) {
            printf("Error allocating memory needed to call GetIfTable\n");
            return 1;
        }
    }
    // Make a second call to GetIfTable to get the actual
    // data we want.
    if ((dwRetVal = GetIfTable(pIfTable, &amp;dwSize, FALSE)) == NO_ERROR) {
        printf("\tNum Entries: %ld\n\n", pIfTable-&gt;dwNumEntries);
        for (i = 0; i &lt; pIfTable-&gt;dwNumEntries; i++) {
            pIfRow = (MIB_IFROW *) &amp; pIfTable-&gt;table[i];
            printf("\tIndex[%d]:\t %ld\n", i, pIfRow-&gt;dwIndex);
            printf("\tInterfaceName[%d]:\t %ws", i, pIfRow-&gt;wszName);
            printf("\n");
            printf("\tDescription[%d]:\t ", i);
            for (j = 0; j &lt; pIfRow-&gt;dwDescrLen; j++)
                printf("%c", pIfRow-&gt;bDescr[j]);
            printf("\n");
            printf("\tType[%d]:\t ", i);
            switch (pIfRow-&gt;dwType) {
            case IF_TYPE_OTHER:
                printf("Other\n");
                break;
            case IF_TYPE_ETHERNET_CSMACD:
                printf("Ethernet\n");
                break;
            case IF_TYPE_ISO88025_TOKENRING:
                printf("Token Ring\n");
                break;
            case IF_TYPE_PPP:
                printf("PPP\n");
                break;
            case IF_TYPE_SOFTWARE_LOOPBACK:
                printf("Software Lookback\n");
                break;
            case IF_TYPE_ATM:
                printf("ATM\n");
                break;
            case IF_TYPE_IEEE80211:
                printf("IEEE 802.11 Wireless\n");
                break;
            case IF_TYPE_TUNNEL:
                printf("Tunnel type encapsulation\n");
                break;
            case IF_TYPE_IEEE1394:
                printf("IEEE 1394 Firewire\n");
                break;
            default:
                printf("Unknown type %ld\n", pIfRow-&gt;dwType);
                break;
            }
            printf("\tMtu[%d]:\t\t %ld\n", i, pIfRow-&gt;dwMtu);
            printf("\tSpeed[%d]:\t %ld\n", i, pIfRow-&gt;dwSpeed);
            printf("\tPhysical Addr:\t ");
            if (pIfRow-&gt;dwPhysAddrLen == 0)
                printf("\n");
            for (j = 0; j &lt; pIfRow-&gt;dwPhysAddrLen; j++) {
                if (j == (pIfRow-&gt;dwPhysAddrLen - 1))
                    printf("%.2X\n", (int) pIfRow-&gt;bPhysAddr[j]);
                else
                    printf("%.2X-", (int) pIfRow-&gt;bPhysAddr[j]);
            }
            printf("\tAdmin Status[%d]:\t %ld\n", i, pIfRow-&gt;dwAdminStatus);
            printf("\tOper Status[%d]:\t ", i);
            switch (pIfRow-&gt;dwOperStatus) {
            case IF_OPER_STATUS_NON_OPERATIONAL:
                printf("Non Operational\n");
                break;
            case IF_OPER_STATUS_UNREACHABLE:
                printf("Unreachable\n");
                break;
            case IF_OPER_STATUS_DISCONNECTED:
                printf("Disconnected\n");
                break;
            case IF_OPER_STATUS_CONNECTING:
                printf("Connecting\n");
                break;
            case IF_OPER_STATUS_CONNECTED:
                printf("Connected\n");
                break;
            case IF_OPER_STATUS_OPERATIONAL:
                printf("Operational\n");
                break;
            default:
                printf("Unknown status %ld\n", pIfRow-&gt;dwAdminStatus);
                break;
            }
            printf("\n");
        }
    } else {
        printf("GetIfTable failed with error: \n", dwRetVal);
        if (pIfTable != NULL) {
            FREE(pIfTable);
            pIfTable = NULL;
        }  
        return 1;
        // Here you can use FormatMessage to find out why 
        // it failed.
    }
    if (pIfTable != NULL) {
        FREE(pIfTable);
        pIfTable = NULL;
    }
    return 0;
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bf16588d-3756-469e-afa2-e2e3dd537047">GetIfEntry</a>



<a href="https://msdn.microsoft.com/da787dae-5e89-4bf2-a9b6-90e727995414">GetIfEntry2</a>



<a href="https://msdn.microsoft.com/0153c41c-b02b-4832-87b3-88dc3a9f4ff1">GetIfTable2</a>



<a href="https://msdn.microsoft.com/d8663894-50b1-4ca2-a1f4-6ca0970795a7">GetIfTable2Ex</a>



<a href="https://msdn.microsoft.com/655d63eb-455a-4a5e-97e2-7b7588eee4d9">GetNumberOfInterfaces</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a>



<a href="https://msdn.microsoft.com/7c3ca3d0-b6fe-4e1c-858f-82ffb26622e7">MIB_IFTABLE</a>



<a href="https://msdn.microsoft.com/e8bb79f9-e7e9-470b-8883-36d08061661b">MIB_IF_ROW2</a>



<a href="https://msdn.microsoft.com/334078c6-afd0-4c53-838c-28bc3e1e8484">MIB_IF_TABLE2</a>
 

 

