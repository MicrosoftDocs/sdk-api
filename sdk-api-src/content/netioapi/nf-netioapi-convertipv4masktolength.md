---
UID: NF:netioapi.ConvertIpv4MaskToLength
title: ConvertIpv4MaskToLength function (netioapi.h)
description: Converts an IPv4 subnet mask to an IPv4 prefix length.
helpviewer_keywords: ["ConvertIpv4MaskToLength","ConvertIpv4MaskToLength function [IP Helper]","iphlp.convertipv4masktolength","netioapi/ConvertIpv4MaskToLength"]
old-location: iphlp\convertipv4masktolength.htm
tech.root: IpHlp
ms.assetid: 63a3c558-24e0-41ef-9417-a3b6b2075977
ms.date: 12/05/2018
ms.keywords: ConvertIpv4MaskToLength, ConvertIpv4MaskToLength function [IP Helper], iphlp.convertipv4masktolength, netioapi/ConvertIpv4MaskToLength
f1_keywords:
- netioapi/ConvertIpv4MaskToLength
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Iphlpapi.dll
api_name:
- ConvertIpv4MaskToLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ConvertIpv4MaskToLength function


## -description


The 
<b>ConvertIpv4MaskToLength</b> function converts an IPv4 subnet mask to an IPv4  prefix length.


## -parameters




### -param Mask [in]

The IPv4 subnet mask.


### -param MaskLength [out]

A pointer to a <b>UINT8</b> value to hold the IPv4 prefix length, in bits, when the function returns successfully.


## -returns



On success, 
<b>ConvertIpv4MaskToLength</b> returns <b>NO_ERROR</b>. Any nonzero return value indicates failure. 

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
One of the parameters was invalid. This error is returned if the <i>Mask</i> parameter was invalid.

</td>
</tr>
</table>
 




## -remarks



The <b>ConvertIpv4MaskToLength</b> function is available on Windows Vista and later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-convertlengthtoipv4mask">ConvertLengthToIpv4Mask</a>
 

 

