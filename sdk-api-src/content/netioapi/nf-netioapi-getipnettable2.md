---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetIpNetTable2 function


## -description


The 
<b>GetIpNetTable2</b> function retrieves the IP neighbor table on the local computer.


## -parameters




### -param Family [in]

The address family to retrieve.

Possible values for the address family are listed in the <i>Winsock2.h</i> header file. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and possible values for this member are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b>, <b>AF_INET6</b>, and <b>AF_UNSPEC</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_UNSPEC"></a><a id="af_unspec"></a><dl>
<dt><b>AF_UNSPEC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The address family is unspecified. When this parameter is specified,  this function  returns the neighbor IP address table containing both IPv4 and IPv6 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family. When this parameter is specified,  this function  returns the neighbor IP address table containing only  IPv4 entries.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family. When this parameter is specified,  this function  returns the neighbor IP address table containing only IPv6 entries. 

</td>
</tr>
</table>
 


### -param Table [out]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559267">MIB_IPNET_TABLE2</a> structure that contains a table of neighbor IP address entries on the local computer. 


## -returns



If the function succeeds, the return value is NO_ERROR or ERROR_NOT_FOUND.

If the function fails or returns no data, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Table</i> parameter or the <i>Family</i> parameter was not specified as <b>AF_INET</b>, <b>AF_INET6</b>, or <b>AF_UNSPEC</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory resources are available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No neighbor IP address entries as specified in the <i>Family</i> parameter were found.  

This return value indicates that the call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552551">GetIpNetTable2</a> function succeeded, but there was no data to return. This can occur when AF_INET is specified in the <i>Family</i> parameter and there are no ARP entries to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. 

This error is returned if no IPv4 stack is on the local computer and <b>AF_INET</b> was specified in the <b>Family</b> parameter. This error is also returned if no IPv6 stack is on the local computer and <b>AF_INET6</b> was specified in the <b>Family</b> parameter. This error is also returned on versions of Windows where this function is not supported.

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



The <b>GetIpNetTable2</b> function is defined on Windows Vista and later. 

The  
<b>GetIpNetTable2</b> function enumerates the neighbor IP addresses on a local system and returns this information in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559267">MIB_IPNET_TABLE2</a> structure. 

The neighbor IP address entries are returned in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559267">MIB_IPNET_TABLE2</a> structure in the buffer pointed to by the <i>Table</i> parameter. The <b>MIB_IPNET_TABLE2</b> structure contains a neighbor IP address entry count and an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> structures for each neighbor IP address entry. When these returned structures are no longer required, free the memory by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550045">FreeMibTable</a>.

The <i>Family</i> parameter must be initialized to either <b>AF_INET</b>,  <b>AF_INET6</b>, or <b>AF_UNSPEC</b>. 

Note that the returned <a href="https://msdn.microsoft.com/library/windows/hardware/ff559267">MIB_IPNET_TABLE2</a> structure pointed to by the <i>Table</i> parameter may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> array entry in the <b>Table</b> member of the <b>MIB_IPNET_TABLE2</b> structure. Padding for alignment may also be present between the <b>MIB_IPNET_ROW2</b> array entries. Any access to a <b>MIB_IPNET_ROW2</b> array entry should assume  padding may exist. 




#### Examples

The following example retrieves the IP neighbor table, then prints the values for IP neighbor row entries in the table.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include &lt;windows.h&gt;
#include &lt;winsock2.h&gt;
#include &lt;ws2ipdef.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

int main()
{

    // Declare and initialize variables

    int i;
    unsigned int j;
    unsigned long status = 0;

    PMIB_IPNET_TABLE2 pipTable = NULL;
//    MIB_IPNET_ROW2 ipRow;

    status = GetIpNetTable2(AF_INET, &amp;pipTable);
    if (status != NO_ERROR) {
        printf("GetIpNetTable for IPv4 table returned error: %ld\n", status);
        exit(1);
    }
    // Print some variables from the table
    printf("Number of IPv4 table entries: %d\n\n", pipTable-&gt;NumEntries);

    for (i = 0; (unsigned) i &lt; pipTable-&gt;NumEntries; i++) {
//        printf("Table entry: %d\n", i);
        printf("IPv4 Address[%d]:\t %s\n", (int) i,
               inet_ntoa(pipTable-&gt;Table[i].Address.Ipv4.sin_addr));
        printf("Interface index[%d]:\t\t %lu\n", (int) i,
               pipTable-&gt;Table[i].InterfaceIndex);

        printf("Interface LUID NetLuidIndex[%d]:\t %lu\n",
               (int) i, pipTable-&gt;Table[i].InterfaceLuid.Info.NetLuidIndex);
        printf("Interface LUID IfType[%d]: ", (int) i);
        switch (pipTable-&gt;Table[i].InterfaceLuid.Info.IfType) {
        case IF_TYPE_OTHER:
            printf("Other\n");
            break;
        case IF_TYPE_ETHERNET_CSMACD:
            printf("Ethernet\n");
            break;
        case IF_TYPE_ISO88025_TOKENRING:
            printf("Token ring\n");
            break;
        case IF_TYPE_PPP:
            printf("PPP\n");
            break;
        case IF_TYPE_SOFTWARE_LOOPBACK:
            printf("Software loopback\n");
            break;
        case IF_TYPE_ATM:
            printf("ATM\n");
            break;
        case IF_TYPE_IEEE80211:
            printf("802.11 wireless\n");
            break;
        case IF_TYPE_TUNNEL:
            printf("Tunnel encapsulation\n");
            break;
        case IF_TYPE_IEEE1394:
            printf("IEEE 1394 (Firewire)\n");
            break;
        default:
            printf("Unknown: %d\n",
                   pipTable-&gt;Table[i].InterfaceLuid.Info.IfType);
            break;
        }

        printf("Physical Address[%d]:\t ", (int) i);
        if (pipTable-&gt;Table[i].PhysicalAddressLength == 0)
            printf("\n");
//        for (j = 0; (unsigned) j &lt; pipTable-&gt;Table[i].PhysicalAddressLength; j++)
//         printf ("%c" 
        for (j = 0; j &lt; pipTable-&gt;Table[i].PhysicalAddressLength; j++) {
            if (j == (pipTable-&gt;Table[i].PhysicalAddressLength - 1))
                printf("%.2X\n", (int) pipTable-&gt;Table[i].PhysicalAddress[j]);
            else
                printf("%.2X-", (int) pipTable-&gt;Table[i].PhysicalAddress[j]);
        }

        printf("Physical Address Length[%d]:\t %lu\n", (int) i,
               pipTable-&gt;Table[i].PhysicalAddressLength);

        printf("Neighbor State[%d]:\t ", (int) i);
        switch (pipTable-&gt;Table[i].State) {
        case NlnsUnreachable:
            printf("NlnsUnreachable\n");
            break;
        case NlnsIncomplete:
            printf("NlnsIncomplete\n");
            break;
        case NlnsProbe:
            printf("NlnsProbe\n");
            break;
        case NlnsDelay:
            printf("NlnsDelay\n");
            break;
        case NlnsStale:
            printf("NlnsStale\n");
            break;
        case NlnsReachable:
            printf("NlnsReachable\n");
            break;
        case NlnsPermanent:
            printf("NlnsPermanent\n");
            break;
        default:
            printf("Unknown: %d\n", pipTable-&gt;Table[i].State);
            break;
        }

        printf("Flags[%d]:\t\t %u\n", (int) i,
               (unsigned char) pipTable-&gt;Table[i].Flags);

        printf("ReachabilityTime[%d]:\t %lu\n\n", (int) i,
               pipTable-&gt;Table[i].ReachabilityTime);

    }
    FreeMibTable(pipTable);
    pipTable = NULL;

    exit(0);
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546217">CreateIpNetEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550029">FlushIpNetTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550045">FreeMibTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552546">GetIpNetEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559267">MIB_IPNET_TABLE2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570686">ResolveIpNetEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570775">SetIpNetEntry2</a>
 

 

