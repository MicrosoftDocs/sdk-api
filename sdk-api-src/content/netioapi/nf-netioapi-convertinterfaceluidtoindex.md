---
UID: NF:netioapi.ConvertInterfaceLuidToIndex
title: ConvertInterfaceLuidToIndex function (netioapi.h)
description: Converts a locally unique identifier (LUID) for a network interface to the local index for the interface.
helpviewer_keywords: ["ConvertInterfaceLuidToIndex","ConvertInterfaceLuidToIndex function [IP Helper]","iphlp.convertinterfaceluidtoindex","netioapi/ConvertInterfaceLuidToIndex"]
old-location: iphlp\convertinterfaceluidtoindex.htm
tech.root: IpHlp
ms.assetid: 904cd94c-dd46-42ac-aef2-ffed4b3e5899
ms.date: 12/05/2018
ms.keywords: ConvertInterfaceLuidToIndex, ConvertInterfaceLuidToIndex function [IP Helper], iphlp.convertinterfaceluidtoindex, netioapi/ConvertInterfaceLuidToIndex
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
 - ConvertInterfaceLuidToIndex
 - netioapi/ConvertInterfaceLuidToIndex
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
 - ConvertInterfaceLuidToIndex
---

# ConvertInterfaceLuidToIndex function


## -description

The 
<b>ConvertInterfaceLuidToIndex</b> function converts a locally unique identifier (LUID) for a network interface to the local index  for the interface.

## -parameters

### -param InterfaceLuid [in]

A pointer to a <a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a> for a network interface.

### -param InterfaceIndex [out]

The local index  value for the interface.

## -returns

On success, 
<b>ConvertInterfaceLuidToIndex</b> returns NO_ERROR. Any nonzero return value indicates failure and a <b>NET_IFINDEX_UNSPECIFIED</b> is returned in the <i>InterfaceIndex</i> parameter. 

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
One of the parameters was invalid. This error is returned if either the <i>InterfaceLuid</i> or <i>InterfaceIndex</i> parameter was <b>NULL</b> or if the <i>InterfaceLuid</i> parameter was invalid. 

</td>
</tr>
</table>

## -remarks

The <b>ConvertInterfaceLuidToIndex</b> function is available on Windows Vista and later.

The <b>ConvertInterfaceLuidToIndex</b> function is protocol independent and works with network interfaces for both the IPv6 and IPv4 protocol.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacealiastoluid">ConvertInterfaceAliasToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceguidtoluid">ConvertInterfaceGuidToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceindextoluid">ConvertInterfaceIndexToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoalias">ConvertInterfaceLuidToAlias</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoguid">ConvertInterfaceLuidToGuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamea">ConvertInterfaceLuidToNameA</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamew">ConvertInterfaceLuidToNameW</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluida">ConvertInterfaceNameToLuidA</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluidw">ConvertInterfaceNameToLuidW</a>



<a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-if_indextoname">if_indextoname</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-if_nametoindex">if_nametoindex</a>