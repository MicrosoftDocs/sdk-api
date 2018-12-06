---
UID: NF:gdiplusgraphics.Graphics.IsVisible
title: Graphics::IsVisible
author: windows-sdk-content
description: This topic lists the IsVisible methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics.
old-location: gdiplus\_gdiplus_CLASS_Graphics_IsVisible_Methods.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsisvisiblemethods.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Graphics.IsVisible, Graphics::IsVisible, IsVisible, IsVisible methods [GDI+], _gdiplus_CLASS_Graphics_IsVisible_Methods, gdiplus._gdiplus_CLASS_Graphics_IsVisible_Methods, gdiplusgraphics/IsVisible
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusgraphics.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics.IsVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Graphics::IsVisible


## -description


<span>This topic lists the 
IsVisible methods of the 
<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> class. For a complete list of methods for the 
<b>Graphics</b> class, see 
<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>. 


</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3280e20-6678-4da1-b5ee-bf920f59cd9b">IsVisible(Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c3280e20-6678-4da1-b5ee-bf920f59cd9b">Graphics::IsVisible</a> method determines whether the specified rectangle intersects the visible clipping region of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this <b>Graphics</b> object and the clipping region of the window.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a290356a-e7d6-4a79-b073-b973c0b44b67">IsVisible(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a290356a-e7d6-4a79-b073-b973c0b44b67">Graphics::IsVisible</a> method determines whether the specified point is inside the visible clipping region of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this <b>Graphics</b> object and the clipping region of the window.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bca16d61-e4ff-4a27-a40d-b2f23f0ba62e">IsVisible(RectF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/bca16d61-e4ff-4a27-a40d-b2f23f0ba62e">Graphics::IsVisible</a> method determines whether the specified rectangle intersects the visible clipping region of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this <b>Graphics</b> object and the clipping region of the window.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81cadd52-1976-4328-85ca-e89aa5b649b5">IsVisible(INT,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/81cadd52-1976-4328-85ca-e89aa5b649b5">Graphics::IsVisible</a>
<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a><b>Graphics</b> object and the clipping region of the window.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88186a93-bfbb-43fb-b872-f638f421a443">IsVisible(PointF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/88186a93-bfbb-43fb-b872-f638f421a443">Graphics::IsVisible</a>
<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a><b>Graphics</b> object and the clipping region of the window.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5602479-dc3a-42c4-968f-10e1e32014ca">IsVisible(REAL,REAL)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a5602479-dc3a-42c4-968f-10e1e32014ca">Graphics::IsVisible</a> method determines whether the specified point is inside the visible clipping region of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this <b>Graphics</b> object and the clipping region of the window.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3b9a42d-ff8d-4839-9aa0-810ccfc26a84">IsVisible(INT,INT,INT,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b3b9a42d-ff8d-4839-9aa0-810ccfc26a84">Graphics::IsVisible</a> method determines whether the specified rectangle intersects the visible clipping region of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The visible clipping region is the intersection of the clipping region of this <b>Graphics</b> object and the clipping region of the window.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64fc22ff-4689-40d6-87ad-8c181a95111e">IsVisible(REAL,REAL,REAL,REAL)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/64fc22ff-4689-40d6-87ad-8c181a95111e">Graphics::IsVisible</a>
<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a><b>Graphics</b> object and the clipping region of the window.

</td>
</tr>
</table>

## -parameters

