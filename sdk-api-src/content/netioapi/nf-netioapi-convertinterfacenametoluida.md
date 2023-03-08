---
UID: NF:netioapi.ConvertInterfaceNameToLuidA
title: ConvertInterfaceNameToLuidA function (netioapi.h)
description: Converts an ANSI network interface name to the locally unique identifier (LUID) for the interface.
helpviewer_keywords: ["ConvertInterfaceNameToLuidA", "ConvertInterfaceNameToLuidA function [IP Helper]", "iphlp.convertinterfacenametoluida", "netioapi/ConvertInterfaceNameToLuidA"]
old-location: iphlp\convertinterfacenametoluida.htm
tech.root: IpHlp
ms.assetid: daceabf9-ff43-4206-9f8f-f3924de9c5a5
ms.date: 12/05/2018
ms.keywords: ConvertInterfaceNameToLuidA, ConvertInterfaceNameToLuidA function [IP Helper], iphlp.convertinterfacenametoluida, netioapi/ConvertInterfaceNameToLuidA
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
 - ConvertInterfaceNameToLuidA
 - netioapi/ConvertInterfaceNameToLuidA
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
 - ConvertInterfaceNameToLuidA
---

# ConvertInterfaceNameToLuidA function


## -description

The 
<b>ConvertInterfaceNameToLuidA</b> function converts an ANSI network interface name to the locally unique identifier (LUID) for the interface.

## -parameters

### -param InterfaceName [in]

A pointer to a <b>NULL</b>-terminated ANSI string containing the network interface name.

### -param InterfaceLuid [out]

A pointer to the <a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a> for this interface.

## -returns

On success, 
<b>ConvertInterfaceNameToLuidA</b> returns <b>NETIO_ERROR_SUCCESS</b>. Any nonzero return value indicates failure. 

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The length of the ANSI interface name was invalid.  This error is returned if the <i>InterfaceName</i> parameter exceeded the maximum allowed string length for this parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The interface name was invalid.  This error is returned if the <i>InterfaceName</i> parameter contained an invalid name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters was invalid. This error is returned if the <i>InterfaceLuid</i> parameter was <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>ConvertInterfaceNameToLuidA</b> function is available on Windows Vista and later.

The <b>ConvertInterfaceNameToLuidA</b> function is protocol independent and works with network interfaces for both the IPv6 and IPv4 protocol. The <b>ConvertInterfaceNameToLuidA</b> converts an ANSI interface name to a LUID. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluidw">ConvertInterfaceNameToLuidW</a> converts a Unicode interface name to a LUID. 

The maximum length of an interface name, <b>NDIS_IF_MAX_STRING_SIZE</b>, without the terminating <b>NULL</b> is declared in the <i>Ntddndis.h</i> header file. The <b>NDIS_IF_MAX_STRING_SIZE</b> is defined to be the <b>IF_MAX_STRING_SIZE</b> constant defined in the <i>Ifdef.h</i> header file. The <i>Ntddndis.h</i> and <i>Ifdef.h</i> header files are automatically included in the <i>Netioapi.h</i> header file which is automatically included by the <i>Iphlpapi.h</i> header file. The <i>Ntddndis.h</i>, <i>Ifdef.h</i>, and <i> Netioapi.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacealiastoluid">ConvertInterfaceAliasToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceguidtoluid">ConvertInterfaceGuidToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceindextoluid">ConvertInterfaceIndexToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoalias">ConvertInterfaceLuidToAlias</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoguid">ConvertInterfaceLuidToGuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoindex">ConvertInterfaceLuidToIndex</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamea">ConvertInterfaceLuidToNameA</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamew">ConvertInterfaceLuidToNameW</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluidw">ConvertInterfaceNameToLuidW</a>



<a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-if_indextoname">if_indextoname</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-if_nametoindex">if_nametoindex</a>
