---
UID: NF:netioapi.ConvertInterfaceLuidToNameW
title: ConvertInterfaceLuidToNameW function (netioapi.h)
description: Converts a locally unique identifier (LUID) for a network interface to the Unicode interface name.
helpviewer_keywords: ["ConvertInterfaceLuidToNameW", "ConvertInterfaceLuidToNameW function [IP Helper]", "iphlp.convertinterfaceluidtonamew", "netioapi/ConvertInterfaceLuidToNameW"]
old-location: iphlp\convertinterfaceluidtonamew.htm
tech.root: IpHlp
ms.assetid: e4269a6a-1237-4503-b7d7-756388458750
ms.date: 12/05/2018
ms.keywords: ConvertInterfaceLuidToNameW, ConvertInterfaceLuidToNameW function [IP Helper], iphlp.convertinterfaceluidtonamew, netioapi/ConvertInterfaceLuidToNameW
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
 - ConvertInterfaceLuidToNameW
 - netioapi/ConvertInterfaceLuidToNameW
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
 - ConvertInterfaceLuidToNameW
---

# ConvertInterfaceLuidToNameW function


## -description

The 
<b>ConvertInterfaceLuidToNameW</b> function converts a locally unique identifier (LUID) for a network interface to the Unicode interface name.

## -parameters

### -param InterfaceLuid [in]

A pointer to a <a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a> for a network interface.

### -param InterfaceName [out]

A pointer to a buffer to hold the <b>NULL</b>-terminated Unicode string containing the interface name when the function returns successfully.

### -param Length [in]

The number of characters in the array pointed to by the <i>InterfaceName</i> parameter. This value must be large enough to accommodate the interface name
        and the terminating null character.  The maximum required length is
        <b>NDIS_IF_MAX_STRING_SIZE</b> + 1.

## -returns

On success, 
<b>ConvertInterfaceLuidToNameW</b> returns <b>NETIO_ERROR_SUCCESS</b>. Any nonzero return value indicates failure. 

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters was invalid. This error is returned if either the <i>InterfaceLuid</i> or the <i>InterfaceName</i> parameter was <b>NULL</b> or if the <i>InterfaceLuid</i> parameter was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
 Not enough storage is available to process this command. This error is returned if the size of the buffer pointed to by <i>InterfaceName</i> parameter was not large enough as specified in the <i>Length</i> parameter to hold the interface name.

</td>
</tr>
</table>

## -remarks

The <b>ConvertInterfaceLuidToNameW</b> function is available on Windows Vista and later.

The <b>ConvertInterfaceLuidToNameW</b> function is protocol independent and works with network interfaces for both the IPv6 and IPv4 protocol. The <b>ConvertInterfaceLuidToNameW</b> converts a network interface LUID to a Unicode interface name.

The <a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamea">ConvertInterfaceLuidToNameA</a> converts an ANSI interface name to a LUID. 

The maximum length of an interface name, <b>NDIS_IF_MAX_STRING_SIZE</b>, without the terminating <b>NULL</b> is declared in the <i>Ntddndis.h</i> header file. The <b>NDIS_IF_MAX_STRING_SIZE</b> is defined to be the <b>IF_MAX_STRING_SIZE</b> constant defined in the <i>Ifdef.h</i> header file. The <i>Ntddndis.h</i> and <i>Ifdef.h</i> header files are automatically included in the <i>Netioapi.h</i> header file which is automatically included by the <i>Iphlpapi.h</i> header file. The <i>Ntddndis.h</i>, <i>Ifdef.h</i>, and <i> Netioapi.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacealiastoluid">ConvertInterfaceAliasToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceguidtoluid">ConvertInterfaceGuidToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceindextoluid">ConvertInterfaceIndexToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoalias">ConvertInterfaceLuidToAlias</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoguid">ConvertInterfaceLuidToGuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoindex">ConvertInterfaceLuidToIndex</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamea">ConvertInterfaceLuidToNameA</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluida">ConvertInterfaceNameToLuidA</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluidw">ConvertInterfaceNameToLuidW</a>



<a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-if_indextoname">if_indextoname</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-if_nametoindex">if_nametoindex</a>
