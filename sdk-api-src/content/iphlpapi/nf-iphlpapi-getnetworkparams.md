---
UID: NF:iphlpapi.GetNetworkParams
title: GetNetworkParams function
author: windows-driver-content
description: The GetNetworkParams function retrieves network parameters for the local computer.
old-location: iphlp\getnetworkparams.htm
old-project: IpHlp
ms.assetid: 5f54a120-5db9-4b8d-a281-1112be0042d6
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetNetworkParams, GetNetworkParams function [IP Helper], _iphlp_getnetworkparams, iphlp.getnetworkparams, iphlpapi/GetNetworkParams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NET_ADDRESS_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	GetNetworkParams
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetNetworkParams function


## -description


The 
<b>GetNetworkParams</b> function retrieves network parameters for the local computer.
		


## -parameters




### -param pFixedInfo [out]

A pointer to a 
buffer that contains a <a href="https://msdn.microsoft.com/6dcf33c6-33dc-4583-9b04-5231948d3d9a">FIXED_INFO</a> structure that receives the network parameters for the local computer, if the function was successful. This buffer must be allocated by the caller prior to calling the <b>GetNetworkParams</b> function.


### -param pOutBufLen [in]

A pointer to a <b>ULONG</b> variable that specifies the size of the 
<a href="https://msdn.microsoft.com/6dcf33c6-33dc-4583-9b04-5231948d3d9a">FIXED_INFO</a> structure. If this size is insufficient to hold the information, 
<b>GetNetworkParams</b> fills in this variable with the required size, and returns an error code of <b>ERROR_BUFFER_OVERFLOW</b>.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The buffer to receive the network parameter information is too small. This value is returned if the <i>pOutBufLen</i> parameter is too small to hold the network parameter information or the <i>pFixedInfo</i> parameter was a <b>NULL</b> pointer. When this error code is returned, the <i>pOutBufLen</i> parameter points to the required buffer size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if the  <i>pOutBufLen</i> parameter is a <b>NULL</b> pointer, the calling process does not have read/write access to the memory pointed to by <i>pOutBufLen</i>, or the calling process does not have write access to the memory pointed to by the <i>pFixedInfo</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
No network parameter information exists for the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <b>GetNetworkParams</b> function is not supported by the operating system running on the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
If the function fails, use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>GetNetworkParams</b> function is used to retrieve  network parameters for the local computer. Network parameters are returned  in a <a href="https://msdn.microsoft.com/6dcf33c6-33dc-4583-9b04-5231948d3d9a">FIXED_INFO</a>
		structure. The  memory for the <b>FIXED_INFO</b>
		structure must be allocated by the application. It is the responsibility of the application to free this memory when it is no longer needed. 

In the Microsoft Windows Software Development Kit (SDK), the <a href="https://msdn.microsoft.com/6dcf33c6-33dc-4583-9b04-5231948d3d9a">FIXED_INFO_WIN2KSP1</a> structure is defined.   When compiling an 
     application if the target platform is Windows 2000 with Service Pack 1 (SP1) and later (<code>NTDDI_VERSION &gt;= NTDDI_WIN2KSP1</code>, 
     <code>_WIN32_WINNT &gt;= 0x0501</code>, or 
     <code>WINVER &gt;= 0x0501</code>), the <b>FIXED_INFO_WIN2KSP1</b> struct is typedefed to the <b>FIXED_INFO</b> structure. When compiling an application if the target 
     platform is not Windows 2000 with SP1 and later, the 
     <b>FIXED_INFO</b> structure is undefined.

The <b>GetNetworkParams</b> function and the 
     <a href="https://msdn.microsoft.com/6dcf33c6-33dc-4583-9b04-5231948d3d9a">FIXED_INFO</a> structure are supported on  Windows 98
  and later. But to build an application for a target platform earlier than Windows 2000 with Service Pack 1 (SP1), an earlier version of the Platform Software Development Kit (SDK)  must be used.


#### Examples

The following example retrieves the network parameters for the local computer and prints information from the returned data.

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




<a href="https://msdn.microsoft.com/6dcf33c6-33dc-4583-9b04-5231948d3d9a">FIXED_INFO</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>
 

 

