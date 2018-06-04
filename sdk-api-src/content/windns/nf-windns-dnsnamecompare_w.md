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

# DnsNameCompare_W function


## -description


The 
<b>DnsNameCompare</b> function compares two DNS names. Like many DNS functions, the 
<b>DnsNameCompare</b> function type is implemented in multiple forms to facilitate different character encoding. Based on the character encoding involved, use one of the following functions:
<ul>
<li>
<b>DnsNameCompare_A</b> (_A for ANSI encoding)

</li>
<li>
<b>DnsNameCompare_W</b> (_W for Unicode encoding)

</li>
<li>
<b>DnsNameCompare_UTF8</b> (_UTF8 for Unicode encoding)

</li>
</ul>

## -parameters




#### - pName1 [in]

A pointer to a string that represents the first DNS name of the comparison pair.


#### - pName2 [in]

A pointer to a string that represents the second DNS name of the comparison pair.


## -returns



Returns <b>TRUE</b> if the compared names are equivalent, <b>FALSE</b> if they are not.




## -remarks



Name comparisons are not case sensitive, and trailing dots are ignored.

As with other DNS comparison functions, the 
<b>DnsNameCompare</b> function deems different encoding as an immediate indication of differing values, and as such, the same names with different characters encoding will not be reported identically.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a>



<a href="https://msdn.microsoft.com/c4449a23-d6d3-4f27-a963-a84144983e5e">DnsRecordCompare</a>



<a href="https://msdn.microsoft.com/008cf2ba-ccb2-430a-85d9-68d424b6938f">DnsRecordSetCompare</a>
 

 

