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

# SetMiterLimit function


## -description


The <b>SetMiterLimit</b> function sets the limit for the length of miter joins for the specified device context.


## -parameters




### -param hdc [in]

Handle to the device context.


### -param limit

TBD


### -param old

TBD




#### - eNewLimit [in]

Specifies the new miter limit for the device context.


#### - peOldLimit [out]

Pointer to a floating-point value that receives the previous miter limit. If this parameter is <b>NULL</b>, the previous miter limit is not returned.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The miter length is defined as the distance from the intersection of the line walls on the inside of the join to the intersection of the line walls on the outside of the join. The miter limit is the maximum allowed ratio of the miter length to the line width.

The default miter limit is 10.0.

<div class="alert"><b>Note</b>  Setting <i>eNewLimit</i> to a float value less than 1.0f will cause the function to fail.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/51b1fb95-dd44-47f8-9311-2c6dc9c57bbc">GetMiterLimit</a>



<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>
 

 

