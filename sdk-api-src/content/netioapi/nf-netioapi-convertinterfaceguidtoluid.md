---
UID: NF:netioapi.ConvertInterfaceGuidToLuid
title: ConvertInterfaceGuidToLuid function (netioapi.h)
description: Converts a globally unique identifier (GUID) for a network interface to the locally unique identifier (LUID) for the interface.
helpviewer_keywords: ["ConvertInterfaceGuidToLuid","ConvertInterfaceGuidToLuid function [IP Helper]","iphlp.convertinterfaceguidtoluid","netioapi/ConvertInterfaceGuidToLuid"]
old-location: iphlp\convertinterfaceguidtoluid.htm
tech.root: IpHlp
ms.assetid: cae669dc-899b-4485-b70a-5f58207a07df
ms.date: 12/05/2018
ms.keywords: ConvertInterfaceGuidToLuid, ConvertInterfaceGuidToLuid function [IP Helper], iphlp.convertinterfaceguidtoluid, netioapi/ConvertInterfaceGuidToLuid
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
 - ConvertInterfaceGuidToLuid
 - netioapi/ConvertInterfaceGuidToLuid
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
 - ConvertInterfaceGuidToLuid
---

# ConvertInterfaceGuidToLuid function


## -description

The 
<b>ConvertInterfaceGuidToLuid</b> function converts a globally unique identifier (GUID) for a network  interface to the locally unique identifier (LUID) for the interface.

## -parameters

### -param InterfaceGuid [in]

A pointer to a GUID for a network interface.

### -param InterfaceLuid [out]

A pointer to the <a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a> for this interface.

## -returns

On success, 
<b>ConvertInterfaceGuidToLuid</b> returns NO_ERROR. Any nonzero return value indicates failure and a <b>NULL</b> is returned in the <i>InterfaceLuid</i> parameter. 

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
One of the parameters was invalid. This error is returned if either the <i>InterfaceAlias</i> or <i>InterfaceLuid</i> parameter was <b>NULL</b> or if the <i>InterfaceGuid</i> parameter was invalid.

</td>
</tr>
</table>

## -remarks

The <b>ConvertInterfaceGuidToLuid</b> function is available on Windows Vista and later.

The <b>ConvertInterfaceGuidToLuid</b> function is protocol independent and works with network interfaces for both the IPv6 and IPv4 protocol.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacealiastoluid">ConvertInterfaceAliasToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceindextoluid">ConvertInterfaceIndexToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoalias">ConvertInterfaceLuidToAlias</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoguid">ConvertInterfaceLuidToGuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoindex">ConvertInterfaceLuidToIndex</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamea">ConvertInterfaceLuidToNameA</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamew">ConvertInterfaceLuidToNameW</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluida">ConvertInterfaceNameToLuidA</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluidw">ConvertInterfaceNameToLuidW</a>



<a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-if_indextoname">if_indextoname</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-if_nametoindex">if_nametoindex</a>