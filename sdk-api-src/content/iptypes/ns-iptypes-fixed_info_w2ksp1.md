---
UID: NS:iptypes.FIXED_INFO_W2KSP1
title: FIXED_INFO_W2KSP1 (iptypes.h)
description: The FIXED_INFO structure contains information that is the same across all the interfaces on a computer.
helpviewer_keywords: ["*PFIXED_INFO","*PFIXED_INFO_W2KSP1","BROADCAST_NODETYPE","FIXED_INFO","FIXED_INFO structure [IP Helper]","FIXED_INFO_W2KSP1","HYBRID_NODETYPE","MIXED_NODETYPE","PEER_TO_PEER_NODETYPE","PFIXED_INFO","PFIXED_INFO structure pointer [IP Helper]","_iphlp_fixed_info","iphlp.fixed_info","iptypes/FIXED_INFO","iptypes/PFIXED_INFO"]
old-location: iphlp\fixed_info.htm
tech.root: IpHlp
ms.assetid: 6dcf33c6-33dc-4583-9b04-5231948d3d9a
ms.date: 12/05/2018
ms.keywords: '*PFIXED_INFO, *PFIXED_INFO_W2KSP1, BROADCAST_NODETYPE, FIXED_INFO, FIXED_INFO structure [IP Helper], FIXED_INFO_W2KSP1, HYBRID_NODETYPE, MIXED_NODETYPE, PEER_TO_PEER_NODETYPE, PFIXED_INFO, PFIXED_INFO structure pointer [IP Helper], _iphlp_fixed_info, iphlp.fixed_info, iptypes/FIXED_INFO, iptypes/PFIXED_INFO'
req.header: iptypes.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FIXED_INFO_W2KSP1, *PFIXED_INFO_W2KSP1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFIXED_INFO_W2KSP1
 - iptypes/PFIXED_INFO_W2KSP1
 - FIXED_INFO_W2KSP1
 - iptypes/FIXED_INFO_W2KSP1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iptypes.h
api_name:
 - FIXED_INFO
---

# FIXED_INFO_W2KSP1 structure


## -description

The 
<b>FIXED_INFO</b> structure contains information that is the same across all the interfaces on a computer.

## -struct-fields

### -field HostName

Type: <b>char[MAX_HOSTNAME_LEN + 4]</b>

The hostname for the local computer. This may be the fully qualified hostname (including the domain) for a computer that is joined to a domain.

### -field DomainName

Type: <b>char[MAX_DOMAIN_NAME_LEN + 4]</b>

The domain in which the local computer is registered.

### -field CurrentDnsServer

Type: <b>PIP_ADDR_STRING</b>

Reserved. Use the <b>DnsServerList</b> member to obtain the DNS servers for the local computer.

### -field DnsServerList

Type: <b>IP_ADDR_STRING</b>

A linked list of 
<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_addr_string">IP_ADDR_STRING</a> structures that specify the set of DNS servers used by the local computer.

### -field NodeType

Type: <b>UINT</b>

The node type of the local computer. These values are defined in the 
      <i>Iptypes.h</i> header file.









<table>
<tr>
<th>NodeType</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BROADCAST_NODETYPE"></a><a id="broadcast_nodetype"></a><dl>
<dt><b>BROADCAST_NODETYPE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
A broadcast nodetype.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_TO_PEER_NODETYPE"></a><a id="peer_to_peer_nodetype"></a><dl>
<dt><b>PEER_TO_PEER_NODETYPE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
A peer to peer nodetype.

</td>
</tr>
<tr>
<td width="40%"><a id="MIXED_NODETYPE"></a><a id="mixed_nodetype"></a><dl>
<dt><b>MIXED_NODETYPE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
A mixed nodetype.

</td>
</tr>
<tr>
<td width="40%"><a id="HYBRID_NODETYPE"></a><a id="hybrid_nodetype"></a><dl>
<dt><b>HYBRID_NODETYPE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
A hybrid nodetype.

</td>
</tr>
</table>

### -field ScopeId

Type: <b>char[MAX_SCOPE_ID_LEN + 4]</b>

The DHCP scope name.

### -field EnableRouting

Type: <b>UINT</b>

A Boolean value that specifies whether routing is enabled on the local computer.

### -field EnableProxy

Type: <b>UINT</b>

A Boolean value that specifies whether the local computer is acting as an ARP proxy.

### -field EnableDns

Type: <b>UINT</b>

A Boolean value that specifies whether DNS is enabled on the local computer.

## -remarks

The 
<b>FIXED_INFO</b> structure is retrieved by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getnetworkparams">GetNetworkParams</a> function.

In the Microsoft Windows Software Development Kit (SDK), the <b>FIXED_INFO_WIN2KSP1</b> structure is defined.   When compiling an 
     application if the target platform is Windows 2000 with Service Pack 1 (SP1) and later (<code>NTDDI_VERSION &gt;= NTDDI_WIN2KSP1</code>, 
     <code>_WIN32_WINNT &gt;= 0x0501</code>, or 
     <code>WINVER &gt;= 0x0501</code>), the <b>FIXED_INFO_WIN2KSP1</b> struct is typedefed to the <b>FIXED_INFO</b> structure. When compiling an application if the target 
     platform is not Windows 2000 with SP1 and later, the 
     <b>FIXED_INFO</b> structure is undefined.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getnetworkparams">GetNetworkParams</a> function and the 
     <b>FIXED_INFO</b> structure are supported on  Windows 98and later. But to build an application for a target platform earlier than Windows 2000 with Service Pack 1 (SP1), an earlier version of the Platform Software Development Kit (SDK)  must be used.


#### Examples

The following code retrieves a 
<b>FIXED_INFO</b> structure that contains network configuration information for the local computer. The code prints selected members from the structure.


```cpp
//
// Link with IPHlpAPI.lib
//
#include <winsock2.h>
#include <iphlpapi.h>
#include <stdio.h>
#include <windows.h>
#pragma comment(lib, "IPHLPAPI.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

/* Note: could also use malloc() and free() */

int __cdecl main()
{

    FIXED_INFO *pFixedInfo;
    ULONG ulOutBufLen;
    DWORD dwRetVal;
    IP_ADDR_STRING *pIPAddr;

    pFixedInfo = (FIXED_INFO *) MALLOC(sizeof (FIXED_INFO));
    if (pFixedInfo == NULL) {
        printf("Error allocating memory needed to call GetNetworkParams\n");
        return 1;
    }
    ulOutBufLen = sizeof (FIXED_INFO);

// Make an initial call to GetAdaptersInfo to get
// the necessary size into the ulOutBufLen variable
    if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
        FREE(pFixedInfo);
        pFixedInfo = (FIXED_INFO *) MALLOC(ulOutBufLen);
        if (pFixedInfo == NULL) {
            printf("Error allocating memory needed to call GetNetworkParams\n");
            return 1;
        }
    }

    if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) == NO_ERROR) {

        printf("Host Name: %s\n", pFixedInfo->HostName);
        printf("Domain Name: %s\n", pFixedInfo->DomainName);

        printf("DNS Servers:\n");
        printf("\t%s\n", pFixedInfo->DnsServerList.IpAddress.String);

        pIPAddr = pFixedInfo->DnsServerList.Next;
        while (pIPAddr) {
            printf("\t%s\n", pIPAddr->IpAddress.String);
            pIPAddr = pIPAddr->Next;
        }

        printf("Node Type: ");
        switch (pFixedInfo->NodeType) {
        case BROADCAST_NODETYPE:
            printf("Broadcast node\n");
            break;
        case PEER_TO_PEER_NODETYPE:
            printf("Peer to Peer node\n");
            break;
        case MIXED_NODETYPE:
            printf("Mixed node\n");
            break;
        case HYBRID_NODETYPE:
            printf("Hybrid node\n");
            break;
        default:
            printf("Unknown node type %0lx\n", pFixedInfo->NodeType);
            break;
        }

        printf("DHCP scope name: %s\n", pFixedInfo->ScopeId);

        if (pFixedInfo->EnableRouting)
            printf("Routing: enabled\n");
        else
            printf("Routing: disabled\n");

        if (pFixedInfo->EnableProxy)
            printf("ARP proxy: enabled\n");
        else
            printf("ARP Proxy: disabled\n");

        if (pFixedInfo->EnableDns)
            printf("DNS: enabled\n");
        else
            printf("DNS: disabled\n");

    } else {
        printf("GetNetworkParams failed with error: %d\n", dwRetVal);
        return 1;
    }

    if (pFixedInfo)
        FREE(pFixedInfo);

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getnetworkparams">GetNetworkParams</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_addr_string">IP_ADDR_STRING</a>

