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

# Graphics::IsVisibleClipEmpty


## -description


The <b>Graphics::IsVisibleClipEmpty</b> method determines whether the visible clipping region of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object is empty. The visible clipping region is the intersection of the clipping region of this <b>Graphics</b> object and the clipping region of the window.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the visible clipping region of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object is empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



If the visible clipping region of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object is empty, there is no area left in which to draw. Consequently, nothing will be drawn when the visible clipping region is empty.


#### Examples



The following example determines whether the visible clipping region is empty. If it is not empty, it draws a rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_IsVisibleClipEmpty(HDC hdc)
{
   Graphics graphics(hdc);

   // If the clipping region is not empty, draw a rectangle.
   if (!graphics.IsVisibleClipEmpty())
   {
   graphics.DrawRectangle(&amp;Pen(Color(255, 0, 0, 0), 3), 0, 0, 100, 100);
   }
}</pre>
</td>
</tr>
</table></span></div>


