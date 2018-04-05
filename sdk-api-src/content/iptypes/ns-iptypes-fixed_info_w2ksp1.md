---
UID: NS:iptypes.FIXED_INFO_W2KSP1
title: FIXED_INFO_W2KSP1
author: windows-driver-content
description: The FIXED_INFO structure contains information that is the same across all the interfaces on a computer.
old-location: iphlp\fixed_info.htm
old-project: IpHlp
ms.assetid: 6dcf33c6-33dc-4583-9b04-5231948d3d9a
ms.author: windowsdriverdev
ms.date: 3/19/2018
ms.keywords: "*PFIXED_INFO, *PFIXED_INFO_W2KSP1, BROADCAST_NODETYPE, FIXED_INFO, FIXED_INFO structure [IP Helper], FIXED_INFO_W2KSP1, HYBRID_NODETYPE, MIXED_NODETYPE, PEER_TO_PEER_NODETYPE, PFIXED_INFO, PFIXED_INFO structure pointer [IP Helper], _iphlp_fixed_info, iphlp.fixed_info, iptypes/FIXED_INFO, iptypes/PFIXED_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iptypes.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FIXED_INFO_W2KSP1, *PFIXED_INFO_W2KSP1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iptypes.h
api_name:
-	FIXED_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/783c383d-7fd3-45bc-90f6-2e8ce01db3c3">IP_ADDR_STRING</a> structures that specify the set of DNS servers used by the local computer.


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
<b>FIXED_INFO</b> structure is retrieved by the <a href="https://msdn.microsoft.com/5f54a120-5db9-4b8d-a281-1112be0042d6">GetNetworkParams</a> function.

In the Microsoft Windows Software Development Kit (SDK), the <b>FIXED_INFO_WIN2KSP1</b> structure is defined.   When compiling an 
     application if the target platform is Windows 2000 with Service Pack 1 (SP1) and later (<code>NTDDI_VERSION &gt;= NTDDI_WIN2KSP1</code>, 
     <code>_WIN32_WINNT &gt;= 0x0501</code>, or 
     <code>WINVER &gt;= 0x0501</code>), the <b>FIXED_INFO_WIN2KSP1</b> struct is typedefed to the <b>FIXED_INFO</b> structure. When compiling an application if the target 
     platform is not Windows 2000 with SP1 and later, the 
     <b>FIXED_INFO</b> structure is undefined.

The <a href="https://msdn.microsoft.com/5f54a120-5db9-4b8d-a281-1112be0042d6">GetNetworkParams</a> function and the 
     <b>FIXED_INFO</b> structure are supported on  Windows 98
  and later. But to build an application for a target platform earlier than Windows 2000 with Service Pack 1 (SP1), an earlier version of the Platform Software Development Kit (SDK)  must be used.


#### Examples

The following code retrieves a 
<b>FIXED_INFO</b> structure that contains network configuration information for the local computer. The code prints selected members from the structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
// Link with IPHlpAPI.lib
//
#include &lt;winsock2.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;
#include &lt;windows.h&gt;
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
    if (GetNetworkParams(pFixedInfo, &amp;ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
        FREE(pFixedInfo);
        pFixedInfo = (FIXED_INFO *) MALLOC(ulOutBufLen);
        if (pFixedInfo == NULL) {
            printf("Error allocating memory needed to call GetNetworkParams\n");
            return 1;
        }
    }

    if (dwRetVal = GetNetworkParams(pFixedInfo, &amp;ulOutBufLen) == NO_ERROR) {

        printf("Host Name: %s\n", pFixedInfo-&gt;HostName);
        printf("Domain Name: %s\n", pFixedInfo-&gt;DomainName);

        printf("DNS Servers:\n");
        printf("\t%s\n", pFixedInfo-&gt;DnsServerList.IpAddress.String);

        pIPAddr = pFixedInfo-&gt;DnsServerList.Next;
        while (pIPAddr) {
            printf("\t%s\n", pIPAddr-&gt;IpAddress.String);
            pIPAddr = pIPAddr-&gt;Next;
        }

        printf("Node Type: ");
        switch (pFixedInfo-&gt;NodeType) {
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
            printf("Unknown node type %0lx\n", pFixedInfo-&gt;NodeType);
            break;
        }

        printf("DHCP scope name: %s\n", pFixedInfo-&gt;ScopeId);

        if (pFixedInfo-&gt;EnableRouting)
            printf("Routing: enabled\n");
        else
            printf("Routing: disabled\n");

        if (pFixedInfo-&gt;EnableProxy)
            printf("ARP proxy: enabled\n");
        else
            printf("ARP Proxy: disabled\n");

        if (pFixedInfo-&gt;EnableDns)
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f54a120-5db9-4b8d-a281-1112be0042d6">GetNetworkParams</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/d53c3821-00a0-4eaa-9a06-69ec7aa98d84">IP Helper Structures</a>



<a href="https://msdn.microsoft.com/783c383d-7fd3-45bc-90f6-2e8ce01db3c3">IP_ADDR_STRING</a>
 

 

