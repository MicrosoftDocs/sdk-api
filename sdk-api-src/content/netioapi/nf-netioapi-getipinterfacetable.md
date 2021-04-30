---
UID: NF:netioapi.GetIpInterfaceTable
title: GetIpInterfaceTable function (netioapi.h)
description: Retrieves the IP interface entries on the local computer.
helpviewer_keywords: ["AF_INET","AF_INET6","AF_UNSPEC","GetIpInterfaceTable","GetIpInterfaceTable function [IP Helper]","iphlp.getipinterfacetable","netioapi/GetIpInterfaceTable"]
old-location: iphlp\getipinterfacetable.htm
tech.root: IpHlp
ms.assetid: 09f2bbff-3281-41ae-878f-61c5afa20ec5
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, AF_UNSPEC, GetIpInterfaceTable, GetIpInterfaceTable function [IP Helper], iphlp.getipinterfacetable, netioapi/GetIpInterfaceTable
req.header: netioapi.h
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetIpInterfaceTable
 - netioapi/GetIpInterfaceTable
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
 - GetIpInterfaceTable
---

# GetIpInterfaceTable function


## -description

The 
<b>GetIpInterfaceTable</b> function  retrieves the IP interface entries on the local computer.

## -parameters

### -param Family [in]

The address family of IP interfaces to retrieve. 

Possible values for the address family are listed in the <i>Winsock2.h</i> header file. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

On Windows Vista and later as well as on the Windows SDK, the organization of header files has changed and possible values for this member are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

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
The address family is unspecified. When this parameter is specified,  the <b>GetIpInterfaceTable</b> function  returns the IP interface table containing both IPv4 and IPv6 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family.

</td>
</tr>
</table>

### -param Table [out]

A pointer to a buffer that receives the table of IP interface entries in a <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_table">MIB_IPINTERFACE_TABLE</a> structure.

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
No IP interface entries as specified in the <i>Family</i> parameter were found. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The function is not supported. This error is returned when the IP transport specified in the <i>Address</i> parameter is not configured on the local computer. This error is also returned on versions of Windows where this function is not supported.

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
the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>GetIpInterfaceTable</b> function is defined on Windows Vista and later. 

The  
<b>GetIpInterfaceTable</b> function enumerates the IP interfaces on a local system and returns this information in an <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_table">MIB_IPINTERFACE_TABLE</a> structure. 

IP interface entries are returned in a <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_table">MIB_IPINTERFACE_TABLE</a> structure in the buffer pointed to by the <i>Table</i> parameter. The <b>MIB_IPINTERFACE_TABLE</b> structure contains an IP interface entry count and an array of <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a> structures for each IP interface entry. When these returned structures are no longer required, free the memory by calling the <a href="/windows/desktop/api/netioapi/nf-netioapi-freemibtable">FreeMibTable</a>.

The <i>Family</i> parameter must be initialized to either <b>AF_INET</b> or <b>AF_INET6</b>. 

Note that the returned <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_table">MIB_IPINTERFACE_TABLE</a> structure pointed to by the <i>Table</i> parameter may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a> array entry in the <b>Table</b> member of the <b>MIB_IPINTERFACE_TABLE</b> structure. Padding for alignment may also be present between the <b>MIB_IPINTERFACE_ROW</b> array entries. Any access to a <b>MIB_IPINTERFACE_ROW</b> array entry should assume  padding may exist. 




#### Examples

The following example retrieves the IP interface table, then prints the values of a few members of the IP interface entries in the table.


```cpp
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2ipdef.h>
#include <iphlpapi.h>
#include <stdio.h>
#include <stdlib.h>

#pragma comment(lib, "iphlpapi.lib")

int main()
{
    // Declare and initialize variables

    int i;

    DWORD dwRetVal = 0;

    PMIB_IPINTERFACE_TABLE pipTable = NULL;

    dwRetVal = GetIpInterfaceTable(AF_UNSPEC, &pipTable);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpInterfaceTable returned error: %ld\n", dwRetVal);
        exit(1);
    }
    // Print some variables from the rows in the table
    printf("Number of table entries: %d\n\n", pipTable->NumEntries);

    for (i = 0; i < (int) pipTable->NumEntries; i++) {
        printf("Address Family[%d]:\t\t", i);
        switch (pipTable->Table[i].Family) {
        case AF_INET:
            printf("IPv4\n");
            break;
        case AF_INET6:
            printf("IPv6\n");
            break;
        default:
            printf("Other: %d\n", pipTable->Table[i].Family);
            break;
        }

        printf("Interface LUID NetLuidIndex[%d]:\t %lu\n",
               i, pipTable->Table[i].InterfaceLuid.Info.NetLuidIndex);

        printf("Interface LUID IfType[%d]:\t ", i);
        switch (pipTable->Table[i].InterfaceLuid.Info.IfType) {
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
                   pipTable->Table[i].InterfaceLuid.Info.IfType);
            break;
        }
        printf("Interface Index[%d]:\t\t %lu\n",
               i, pipTable->Table[i].InterfaceIndex);
        printf("Maximum reassembly size[%d]:\t %lu\n", i,
               pipTable->Table[i].MaxReassemblySize);

        printf("Advertising enabled[%d]:\t\t ", i);
        if (pipTable->Table[i].AdvertisingEnabled)
            printf("Yes\n");
        else
            printf("No\n");

        printf("Forwarding enabled[%d]:\t\t ", i);
        if (pipTable->Table[i].ForwardingEnabled)
            printf("Yes\n");
        else
            printf("No\n");

        printf("Network layer MTU[%d]:\t\t %lu\n", i, pipTable->Table[i].NlMtu);

        printf("Connected[%d]:\t\t\t ", i);
        if (pipTable->Table[i].Connected)
            printf("Yes\n");
        else
            printf("No\n");

        printf("Supports wakeup patterns[%d]:\t ", i);
        if (pipTable->Table[i].SupportsWakeUpPatterns)
            printf("Yes\n");
        else
            printf("No\n");

        printf("Supports neighbor discovery[%d]:\t ", i);
        if (pipTable->Table[i].SupportsNeighborDiscovery)
            printf("Yes\n");
        else
            printf("No\n");

        printf("Supports router discovery[%d]:\t ", i);
        if (pipTable->Table[i].SupportsRouterDiscovery)
            printf("Yes\n");
        else
            printf("No\n");

        printf("\n");
    }

    FreeMibTable(pipTable);
    pipTable = NULL;

    exit(0);
}


```

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-freemibtable">FreeMibTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getifentry2">GetIfEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getifstacktable">GetIfStackTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2">GetIfTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getinvertedifstacktable">GetInvertedIfStackTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-initializeipinterfaceentry">InitializeIpInterfaceEntry</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_table2">MIB_IF_TABLE2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_table">MIB_IPINTERFACE_TABLE</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyipinterfacechange">NotifyIpInterfaceChange</a>