---
UID: NF:iphlpapi.GetIfEntry
title: GetIfEntry function
author: windows-sdk-content
description: The GetIfEntry function retrieves information for the specified interface on the local computer.
old-location: iphlp\getifentry.htm
tech.root: IpHlp
ms.assetid: bf16588d-3756-469e-afa2-e2e3dd537047
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetIfEntry, GetIfEntry function [IP Helper], _iphlp_getifentry, iphlp.getifentry, iphlpapi/GetIfEntry
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - GetIfEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetIfEntry
: 
---

# GetIfEntry function


## -description


The 
<b>GetIfEntry</b> function retrieves information for the specified interface on the local computer.


## -parameters




### -param pIfRow [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a> structure that, on successful return, receives information for an interface on the local computer. On input, set the <b>dwIndex</b> member of <b>MIB_IFROW</b> to the index of the interface for which to retrieve information. The value for the <b>dwIndex</b> must be retrieved by a previous call to the <a href="https://msdn.microsoft.com/6a46c1df-b274-415e-b842-fc1adf6fa206">GetIfTable</a>, <a href="https://msdn.microsoft.com/0153c41c-b02b-4832-87b3-88dc3a9f4ff1">GetIfTable2</a>, or <a href="https://msdn.microsoft.com/d8663894-50b1-4ca2-a1f4-6ca0970795a7">GetIfTable2Ex</a> function.


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
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The request could not be completed. This is an internal error. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The data is invalid. This error is returned if the  network interface index specified by the <b>dwIndex</b>  member of the <a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a> structure pointed to by the <i>pIfRow</i> parameter is not a valid interface index on the local computer.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>pIfRow</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified interface could not be found. This error is returned if the  network interface index specified by the <b>dwIndex</b>  member of the <a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a> structure pointed to by the <i>pIfRow</i> parameter could not be found.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if IPv4 is not configured on the local computer. 

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



The <b>GetIfEntry</b> function retrieves information for an interface on a local computer. 

The <b>dwIndex</b> member in the <a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a> structure pointed to by the <i>pIfRow</i> parameter must be initialized to a valid network interface index retrieved by a previous call to the <a href="https://msdn.microsoft.com/6a46c1df-b274-415e-b842-fc1adf6fa206">GetIfTable</a>, <a href="https://msdn.microsoft.com/0153c41c-b02b-4832-87b3-88dc3a9f4ff1">GetIfTable2</a>, or <a href="https://msdn.microsoft.com/d8663894-50b1-4ca2-a1f4-6ca0970795a7">GetIfTable2Ex</a> function.

The <b>GetIfEntry</b> function will fail if the  <b>dwIndex</b>  member of the <a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a> pointed to by the <i>pIfRow</i> parameter does not match an existing interface index on the local computer. 


#### Examples

The following example retrieves the entries from the interface table and prints some of the information available for that  entry.

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
        exit (1);
    }
    // Before calling GetIfEntry, we call GetIfTable to make
    // sure there are entries to get and retrieve the interface index.

    // Make an initial call to GetIfTable to get the
    // necessary size into dwSize
    dwSize = sizeof (MIB_IFTABLE);
    if (GetIfTable(pIfTable, &amp;dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        FREE(pIfTable);
        pIfTable = (MIB_IFTABLE *) MALLOC(dwSize);
        if (pIfTable == NULL) {
            printf("Error allocating memory\n");
            exit (1);
        }
    }
    // Make a second call to GetIfTable to get the actual
    // data we want.
    if ((dwRetVal = GetIfTable(pIfTable, &amp;dwSize, 0)) == NO_ERROR) {
        if (pIfTable-&gt;dwNumEntries &gt; 0) {
            pIfRow = (MIB_IFROW *) MALLOC(sizeof (MIB_IFROW));
            if (pIfRow == NULL) {
                printf("Error allocating memory\n");
                if (pIfTable != NULL) {
                    FREE(pIfTable);
                    pIfTable = NULL;
                }
                exit (1);
            }

            printf("\tNum Entries: %ld\n\n", pIfTable-&gt;dwNumEntries);
            for (i = 0; i &lt; pIfTable-&gt;dwNumEntries; i++) {
                pIfRow-&gt;dwIndex = pIfTable-&gt;table[i].dwIndex;
                if ((dwRetVal = GetIfEntry(pIfRow)) == NO_ERROR) {
                    printf("\tIndex:\t %ld\n", pIfRow-&gt;dwIndex);
                    printf("\tInterfaceName[%d]:\t ", i);
                    if (pIfRow-&gt;wszName != NULL)
                        printf("%ws", pIfRow-&gt;wszName);
                    printf("\n");

                    printf("\tDescription[%d]:\t ", i);
                    for (j = 0; j &lt; pIfRow-&gt;dwDescrLen; j++)
                        printf("%c", pIfRow-&gt;bDescr[j]);
                    printf("\n");

                    printf("\tIndex[%d]:\t\t %d\n", i, pIfRow-&gt;dwIndex);

                    printf("\tType[%d]:\t\t ", i);
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

                    printf("\tSpeed[%d]:\t\t %ld\n", i, pIfRow-&gt;dwSpeed);

                    printf("\tPhysical Addr:\t\t ");
                    if (pIfRow-&gt;dwPhysAddrLen == 0)
                        printf("\n");
//                    for (j = 0; j &lt; (int) pIfRow-&gt;dwPhysAddrLen; j++) {
                    for (j = 0; j &lt; pIfRow-&gt;dwPhysAddrLen; j++) {
                        if (j == (pIfRow-&gt;dwPhysAddrLen - 1))
                            printf("%.2X\n", (int) pIfRow-&gt;bPhysAddr[j]);
                        else
                            printf("%.2X-", (int) pIfRow-&gt;bPhysAddr[j]);
                    }
                    printf("\tAdmin Status[%d]:\t %ld\n", i,
                           pIfRow-&gt;dwAdminStatus);

                    printf("\tOper Status[%d]:\t ", i);
                    switch (pIfRow-&gt;dwOperStatus) {
                    case IF_OPER_STATUS_NON_OPERATIONAL:
                        printf("Non Operational\n");
                        break;
                    case IF_OPER_STATUS_UNREACHABLE:
                        printf("Unreasonable\n");
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
                        printf("Unknown status %ld\n", 
                            pIfRow-&gt;dwAdminStatus);
                        break;
                    }
                    printf("\n");
                }

                else {
                    printf("GetIfEntry failed for index %d with error: %ld\n",
                           i, dwRetVal);
                    // Here you can use FormatMessage to find out why 
                    // it failed.

                }
            }
        } else {
            printf("\tGetIfTable failed with error: %ld\n", dwRetVal);
        }

    }
    
    exit (0);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/da787dae-5e89-4bf2-a9b6-90e727995414">GetIfEntry2</a>



<a href="https://msdn.microsoft.com/6a46c1df-b274-415e-b842-fc1adf6fa206">GetIfTable</a>



<a href="https://msdn.microsoft.com/0153c41c-b02b-4832-87b3-88dc3a9f4ff1">GetIfTable2</a>



<a href="https://msdn.microsoft.com/d8663894-50b1-4ca2-a1f4-6ca0970795a7">GetIfTable2Ex</a>



<a href="https://msdn.microsoft.com/655d63eb-455a-4a5e-97e2-7b7588eee4d9">GetNumberOfInterfaces</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/b08631e9-6036-4377-b2f2-4ea899acb787">MIB_IFROW</a>



<a href="https://msdn.microsoft.com/7c3ca3d0-b6fe-4e1c-858f-82ffb26622e7">MIB_IFTABLE</a>



<a href="https://msdn.microsoft.com/e8bb79f9-e7e9-470b-8883-36d08061661b">MIB_IF_ROW2</a>



<a href="https://msdn.microsoft.com/334078c6-afd0-4c53-838c-28bc3e1e8484">MIB_IF_TABLE2</a>



<b>SetIfEntry</b>
 

 

