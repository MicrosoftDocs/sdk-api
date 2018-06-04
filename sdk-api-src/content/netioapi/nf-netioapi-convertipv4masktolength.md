---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



The <b>ConvertIpv4MaskToLength</b> function is available on Windows Vista
  
   and later.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546202">ConvertLengthToIpv4Mask</a>
 

 

