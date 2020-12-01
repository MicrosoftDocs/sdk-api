---
UID: NF:netioapi.ConvertLengthToIpv4Mask
title: ConvertLengthToIpv4Mask function (netioapi.h)
description: Converts an IPv4 prefix length to an IPv4 subnet mask.
helpviewer_keywords: ["ConvertLengthToIpv4Mask","ConvertLengthToIpv4Mask function [IP Helper]","iphlp.convertlengthtoipv4mask","netioapi/ConvertLengthToIpv4Mask"]
old-location: iphlp\convertlengthtoipv4mask.htm
tech.root: IpHlp
ms.assetid: 5d986301-368e-4984-9f90-e2af1f87cbea
ms.date: 12/05/2018
ms.keywords: ConvertLengthToIpv4Mask, ConvertLengthToIpv4Mask function [IP Helper], iphlp.convertlengthtoipv4mask, netioapi/ConvertLengthToIpv4Mask
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
 - ConvertLengthToIpv4Mask
 - netioapi/ConvertLengthToIpv4Mask
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
 - ConvertLengthToIpv4Mask
---

# ConvertLengthToIpv4Mask function


## -description

The 
<b>ConvertLengthToIpv4Mask</b> function converts an IPv4  prefix length to an IPv4 subnet mask.

## -parameters

### -param MaskLength [in]

The IPv4 prefix length, in bits.

### -param Mask [out]

A pointer to a <b>LONG</b> value to hold the IPv4 subnet mask when the function returns successfully.

## -returns

On success, 
<b>ConvertLengthToIpv4Mask</b> returns <b>NO_ERROR</b>. Any nonzero return value indicates failure and the <i>Mask</i> parameter is set to <b>INADDR_NONE</b> defined in the <i>Ws2def.h</i> header file. 

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
One of the parameters was invalid. This error is returned if the <i>MaskLength</i> parameter was invalid.

</td>
</tr>
</table>

## -remarks

The <b>ConvertLengthToIpv4Mask</b> function is available on Windows Vista and later.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-convertipv4masktolength">ConvertIpv4MaskToLength</a>