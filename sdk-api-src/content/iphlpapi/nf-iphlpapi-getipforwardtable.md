---
UID: NF:iphlpapi.GetIpForwardTable
title: GetIpForwardTable function (iphlpapi.h)
description: The GetIpForwardTable function retrieves the IPv4 routing table.
helpviewer_keywords: ["GetIpForwardTable","GetIpForwardTable function [IP Helper]","_iphlp_getipforwardtable","iphlp.getipforwardtable","iphlpapi/GetIpForwardTable"]
old-location: iphlp\getipforwardtable.htm
tech.root: IpHlp
ms.assetid: 5d645353-7c87-4f8a-b7fd-149675a94743
ms.date: 12/05/2018
ms.keywords: GetIpForwardTable, GetIpForwardTable function [IP Helper], _iphlp_getipforwardtable, iphlp.getipforwardtable, iphlpapi/GetIpForwardTable
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetIpForwardTable
 - iphlpapi/GetIpForwardTable
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
 - GetIpForwardTable
---

# GetIpForwardTable function


## -description

The 
<b>GetIpForwardTable</b> function retrieves the IPv4 routing table.

## -parameters

### -param pIpForwardTable [out]

A pointer to a buffer that receives the IPv4 routing table as a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardtable">MIB_IPFORWARDTABLE</a> structure.

### -param pdwSize [in, out]

On input, specifies the size in bytes  of the buffer pointed to by the <i>pIpForwardTable</i> parameter. 




On output, if the buffer is not large enough to hold the returned routing table, the function sets this parameter equal to the required buffer size in bytes.

### -param bOrder [in]

A Boolean value that specifies whether the returned table should be sorted. If this parameter is <b>TRUE</b>, the table is sorted in the order of: 


<ol>
<li>Destination address</li>
<li>Protocol that generated the route</li>
<li>Multipath routing policy</li>
<li>Next-hop address</li>
</ol>

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b> (zero).

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
The buffer pointed to by the <i>pIpForwardTable</i> parameter is not large enough. The required size is returned in the <b>DWORD</b> variable pointed to by the <i>pdwSize</i> parameter.

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
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipforwardtable">GetIpForwardTable</a> is unable to write to the memory pointed to by the <i>pdwSize</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
No data is available. This error is returned if there are no routes present on the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function is not supported on the operating system in use on the local system. This error is returned if there is no IP stack installed on the local computer.

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

The  <b>dwForwardProto</b> member of the 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure specifies the protocol or routing mechanism that generated the route. See 
<a href="/windows/desktop/RRAS/protocol-identifiers">Protocol Identifiers</a> for a list of possible protocols and routing mechanisms.

The  <b>dwForwardDest</b>, <b>dwForwardMask</b>, and <b>dwForwardNextHop</b> members of the 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure represent an IPv4 address in network byte order.

An IPv4 address of 0.0.0.0 in the  <b>dwForwardDest</b> member of the 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure is considered a
                default route. The <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardtable">MIB_IPFORWARDTABLE</a> may contain multiple <b>MIB_IPFORWARDROW</b> entries with the <b>dwForwardDest</b> member set to 0.0.0.0 when there are multiple network adapters installed.

When <b>dwForwardAge</b> is set to <b>INFINITE</b>, the route will not be removed based on a timeout
 
value. Any other value for <b>dwForwardAge</b> specifies the number of seconds since the route was added or modified in the network routing table.



On Windows Server 2003 or
  Windows 2000 Server when the Routing and Remote Access Service (RRAS) is running, the  <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> entries returned have the <b>dwForwardType</b> and <b>dwForwardAge</b> members set to zero. 

On Windows Vista and Windows Server 2008, the route metric specified in the <b>dwForwardMetric1</b> member of the  <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure represents a combination of the route metric added to the interface metric specified in the <b>Metric</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a> structure of the associated interface.  So the <b>dwForwardMetric1</b> member of the  <b>MIB_IPFORWARDROW</b> structure should be equal to or greater than <b>Metric</b> member of the associated <b>MIB_IPINTERFACE_ROW</b> structure. If an application would like to set the route metric to 0 on Windows Vista and Windows Server 2008, then the <b>dwForwardMetric1</b> member of the <b>MIB_IPFORWARDROW</b> structure  should be set equal to the value of the interface metric specified in the <b>Metric</b> member of the associated <b>MIB_IPINTERFACE_ROW</b> structure. An application can retrieve the interface metric by calling the <a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a> function.

A number of members of the <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure  entries returned by <b>GetIpForwardTable</b> are not currently used by IPv4 routing. These members include <b>dwForwardPolicy</b>, <b>dwForwardNextHopAS</b>, <b>dwForwardMetric2</b>, <b>dwForwardMetric3</b>, <b>dwForwardMetric4</b>, and <b>dwForwardMetric5</b>. 


#### Examples

The following example retrieves the IP routing table then prints some fields for each route in the table.


```cpp
// Need to link with Ws2_32.lib and Iphlpapi.lib
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

/* Note: could also use malloc() and free() */

int main()
{

    // Declare and initialize variables.

    /* variables used for GetIfForwardTable */
    PMIB_IPFORWARDTABLE pIpForwardTable;
    DWORD dwSize = 0;
    DWORD dwRetVal = 0;

    char szDestIp[128];
    char szMaskIp[128];
    char szGatewayIp[128];

    struct in_addr IpAddr;

    int i;

    pIpForwardTable =
        (MIB_IPFORWARDTABLE *) MALLOC(sizeof (MIB_IPFORWARDTABLE));
    if (pIpForwardTable == NULL) {
        printf("Error allocating memory\n");
        return 1;
    }

    if (GetIpForwardTable(pIpForwardTable, &dwSize, 0) ==
        ERROR_INSUFFICIENT_BUFFER) {
        FREE(pIpForwardTable);
        pIpForwardTable = (MIB_IPFORWARDTABLE *) MALLOC(dwSize);
        if (pIpForwardTable == NULL) {
            printf("Error allocating memory\n");
            return 1;
        }
    }

    /* Note that the IPv4 addresses returned in 
     * GetIpForwardTable entries are in network byte order 
     */
    if ((dwRetVal = GetIpForwardTable(pIpForwardTable, &dwSize, 0)) == NO_ERROR) {
        printf("\tNumber of entries: %d\n",
               (int) pIpForwardTable->dwNumEntries);
        for (i = 0; i < (int) pIpForwardTable->dwNumEntries; i++) {
            /* Convert IPv4 addresses to strings */
            IpAddr.S_un.S_addr =
                (u_long) pIpForwardTable->table[i].dwForwardDest;
            strcpy_s(szDestIp, sizeof (szDestIp), inet_ntoa(IpAddr));
            IpAddr.S_un.S_addr =
                (u_long) pIpForwardTable->table[i].dwForwardMask;
            strcpy_s(szMaskIp, sizeof (szMaskIp), inet_ntoa(IpAddr));
            IpAddr.S_un.S_addr =
                (u_long) pIpForwardTable->table[i].dwForwardNextHop;
            strcpy_s(szGatewayIp, sizeof (szGatewayIp), inet_ntoa(IpAddr));

            printf("\n\tRoute[%d] Dest IP: %s\n", i, szDestIp);
            printf("\tRoute[%d] Subnet Mask: %s\n", i, szMaskIp);
            printf("\tRoute[%d] Next Hop: %s\n", i, szGatewayIp);
            printf("\tRoute[%d] If Index: %ld\n", i,
                   pIpForwardTable->table[i].dwForwardIfIndex);
            printf("\tRoute[%d] Type: %ld - ", i,
                   pIpForwardTable->table[i].dwForwardType);
            switch (pIpForwardTable->table[i].dwForwardType) {
            case MIB_IPROUTE_TYPE_OTHER:
                printf("other\n");
                break;
            case MIB_IPROUTE_TYPE_INVALID:
                printf("invalid route\n");
                break;
            case MIB_IPROUTE_TYPE_DIRECT:
                printf("local route where next hop is final destination\n");
                break;
            case MIB_IPROUTE_TYPE_INDIRECT:
                printf
                    ("remote route where next hop is not final destination\n");
                break;
            default:
                printf("UNKNOWN Type value\n");
                break;
            }
            printf("\tRoute[%d] Proto: %ld - ", i,
                   pIpForwardTable->table[i].dwForwardProto);
            switch (pIpForwardTable->table[i].dwForwardProto) {
            case MIB_IPPROTO_OTHER:
                printf("other\n");
                break;
            case MIB_IPPROTO_LOCAL:
                printf("local interface\n");
                break;
            case MIB_IPPROTO_NETMGMT:
                printf("static route set through network management \n");
                break;
            case MIB_IPPROTO_ICMP:
                printf("result of ICMP redirect\n");
                break;
            case MIB_IPPROTO_EGP:
                printf("Exterior Gateway Protocol (EGP)\n");
                break;
            case MIB_IPPROTO_GGP:
                printf("Gateway-to-Gateway Protocol (GGP)\n");
                break;
            case MIB_IPPROTO_HELLO:
                printf("Hello protocol\n");
                break;
            case MIB_IPPROTO_RIP:
                printf("Routing Information Protocol (RIP)\n");
                break;
            case MIB_IPPROTO_IS_IS:
                printf
                    ("Intermediate System-to-Intermediate System (IS-IS) protocol\n");
                break;
            case MIB_IPPROTO_ES_IS:
                printf("End System-to-Intermediate System (ES-IS) protocol\n");
                break;
            case MIB_IPPROTO_CISCO:
                printf("Cisco Interior Gateway Routing Protocol (IGRP)\n");
                break;
            case MIB_IPPROTO_BBN:
                printf("BBN Internet Gateway Protocol (IGP) using SPF\n");
                break;
            case MIB_IPPROTO_OSPF:
                printf("Open Shortest Path First (OSPF) protocol\n");
                break;
            case MIB_IPPROTO_BGP:
                printf("Border Gateway Protocol (BGP)\n");
                break;
            case MIB_IPPROTO_NT_AUTOSTATIC:
                printf("special Windows auto static route\n");
                break;
            case MIB_IPPROTO_NT_STATIC:
                printf("special Windows static route\n");
                break;
            case MIB_IPPROTO_NT_STATIC_NON_DOD:
                printf
                    ("special Windows static route not based on Internet standards\n");
                break;
            default:
                printf("UNKNOWN Proto value\n");
                break;
            }

            printf("\tRoute[%d] Age: %ld\n", i,
                   pIpForwardTable->table[i].dwForwardAge);
            printf("\tRoute[%d] Metric1: %ld\n", i,
                   pIpForwardTable->table[i].dwForwardMetric1);
        }
        FREE(pIpForwardTable);
        return 0;
    } else {
        printf("\tGetIpForwardTable failed.\n");
        FREE(pIpForwardTable);
        return 1;
    }

}


```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry">CreateIpForwardEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry">DeleteIpForwardEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardtable">MIB_IPFORWARDTABLE</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a>



<a href="/windows/desktop/RRAS/protocol-identifiers">Protocol Identifiers</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry">SetIpForwardEntry</a>