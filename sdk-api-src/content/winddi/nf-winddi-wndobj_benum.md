---
UID: NF:winddi.WNDOBJ_bEnum
title: WNDOBJ_bEnum function
author: windows-sdk-content
description: The WNDOBJ_bEnum function obtains a batch of rectangles from the visible region of a window.
old-location: display\wndobj_benum.htm
tech.root: display
ms.assetid: ad883ab5-6374-499e-9144-e5b85feaa471
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WNDOBJ_bEnum, WNDOBJ_bEnum function [Display Devices], display.wndobj_benum, gdifncs_73e625c4-af7b-4e0e-aace-b930ca192444.xml, winddi/WNDOBJ_bEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - WNDOBJ_bEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WNDOBJ_bEnum function


## -description


The <b>WNDOBJ_bEnum</b> function obtains a batch of rectangles from the visible region of a window.


## -parameters




### -param pwo

Pointer to a <a href="https://msdn.microsoft.com/69c47add-82a7-48fd-ae91-7756a6a8d15b">WNDOBJ</a> structure created by a call to <a href="https://msdn.microsoft.com/14b1cced-32d0-4ba8-be7c-e626bef37e3f">EngCreateWnd</a>.


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



The order of enumeration is determined by the call to <a href="https://msdn.microsoft.com/7d3951de-807f-4d54-a022-e2610987d965">WNDOBJ_cEnumStart</a>.

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
<b>WNDOBJ_bEnum</b> should be called only by the callback function provided to GDI by the <a href="https://msdn.microsoft.com/14b1cced-32d0-4ba8-be7c-e626bef37e3f">EngCreateWnd</a> function, or by the graphics DDI functions that are given a WNDOBJ.




## -see-also




<a href="https://msdn.microsoft.com/14b1cced-32d0-4ba8-be7c-e626bef37e3f">EngCreateWnd</a>



<a href="https://msdn.microsoft.com/69c47add-82a7-48fd-ae91-7756a6a8d15b">WNDOBJ</a>



<a href="https://msdn.microsoft.com/7d3951de-807f-4d54-a022-e2610987d965">WNDOBJ_cEnumStart</a>
 

 

