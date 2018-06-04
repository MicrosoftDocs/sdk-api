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

# CLIPOBJ_bEnum function


## -description


The <b>CLIPOBJ_bEnum</b> function enumerates a batch of rectangles from a specified <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a>; a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539421">CLIPOBJ_cEnumStart</a> determines the order of enumeration.


## -parameters




### -param pco [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure describing the clip region that is to be enumerated.


### -param cj [in]

Specifies the size, in bytes, of the buffer pointed to by <i>pv</i>.


### -param pul

TBD




#### - pv [out]

Pointer to the buffer that will receive data about the clip region in an <a href="https://msdn.microsoft.com/library/windows/hardware/ff565490">ENUMRECTS</a> structure.


## -returns



The return value is <b>TRUE</b> if the driver must call this function again for more enumeration data, or <b>FALSE</b> if the enumeration is complete. It is possible for <b>CLIPOBJ_bEnum</b> to return <b>TRUE</b> with the number of clipping rectangles equal to zero. In such cases, the driver should call <b>CLIPOBJ_bEnum</b> again without taking any action.




## -remarks



A possible loop structure for calling this function follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>do {
    bMore = CLIPOBJ_bEnum(pco, sizeof(buffer), &amp;buffer.c);
    for (i = 0; i &lt; buffer.c; i++) {
        .
        .
        .
    }
} while (bMore);</pre>
</td>
</tr>
</table></span></div>
The count of objects written to the buffer is written to the buffer itself.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539421">CLIPOBJ_cEnumStart</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565490">ENUMRECTS</a>
 

 

