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

# WNDOBJ_bEnum function


## -description


The <b>WNDOBJ_bEnum</b> function obtains a batch of rectangles from the visible region of a window.


## -parameters




### -param pwo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a> structure created by a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>.


### -param cj

Specifies the size, in bytes, of the buffer pointed to by <i>pul</i>. GDI will not write beyond this limit.


### -param pul

Pointer to the buffer in which a structure of the following form is to be written. In this structure, <b>c</b> is a count of the rectangles returned, and <b>arcl</b> is an array of rectangles:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef struct _ENUMRECTS{
    ULONG c;
    RECTL arcl[]
} ENUMRECTS;</pre>
</td>
</tr>
</table></span></div>

## -returns



The return value is <b>TRUE</b> if there is more data to be enumerated and the driver should repeat the call. It is <b>FALSE</b> if the enumeration is complete.




## -remarks



The order of enumeration is determined by the call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff570603">WNDOBJ_cEnumStart</a>.

A possible loop structure for calling this function follows.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>do {
    bMore = WNDOBJ_bEnum(pwo, sizeof(buffer), &amp;buffer.c);
    for (i = 0; i &lt; buffer.c; i++) { 
        //  Process the data
    }
} while (bMore);</pre>
</td>
</tr>
</table></span></div>
<b>WNDOBJ_bEnum</b> should be called only by the callback function provided to GDI by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a> function, or by the graphics DDI functions that are given a WNDOBJ.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570603">WNDOBJ_cEnumStart</a>
 

 

