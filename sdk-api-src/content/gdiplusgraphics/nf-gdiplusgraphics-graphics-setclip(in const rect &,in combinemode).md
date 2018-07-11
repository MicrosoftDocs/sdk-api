---
UID: NF:gdiplusgraphics.Graphics.SetClip(IN const Rect &,IN CombineMode)
title: Graphics::SetClip(IN const Rect &,IN CombineMode)
author: windows-sdk-content
description: This topic lists the SetClip methods of the Graphics class. For a complete list of methods for the Graphics class, see Graphics.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetClip_Methods.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicssetclipmethods.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Graphics.SetClip, Graphics.SetClip(IN const Rect &,IN CombineMode), Graphics::SetClip, Graphics::SetClip(IN const Rect &,IN CombineMode), SetClip, SetClip methods [GDI+], _gdiplus_CLASS_Graphics_SetClip_Methods, gdiplus._gdiplus_CLASS_Graphics_SetClip_Methods, gdiplusgraphics/SetClip
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics.SetClip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::SetClip(IN const Rect &,IN CombineMode)


## -description


<span>This topic lists the 
SetClip methods of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> class. For a complete list of methods for the 
<b>Graphics</b> class, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>. 


</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0968120f-ab5d-4f04-bf55-3e6fefc52336">SetClip(HRGN,CombineMode)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0968120f-ab5d-4f04-bf55-3e6fefc52336">Graphics::SetClip</a> method updates the clipping region of this  <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to a region that is the combination of itself and a GDI region.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d014787c-081c-4490-b364-dc6d5a9b6ee7">SetClip(Rect&,CombineMode)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d014787c-081c-4490-b364-dc6d5a9b6ee7">Graphics::SetClip</a> method updates the clipping region of this  <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to a region that is the combination of itself and a rectangle.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a39ef640-a286-4007-9cec-2b4f1f72e6db">SetClip(RectF&,CombineMode)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a39ef640-a286-4007-9cec-2b4f1f72e6db">Graphics::SetClip</a> method updates the clipping region of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to a region that is the combination of itself and a rectangle.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ca20e14-acc4-45f4-a293-04f12bd7a0a4">SetClip(Region*,CombineMode)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2ca20e14-acc4-45f4-a293-04f12bd7a0a4">Graphics::SetClip</a> method updates the clipping region of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to a region that is the combination of itself and the region specified by a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a> object.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77ca4449-3bd3-4476-9502-6b05638ecf7f">SetClip(Graphics*,CombineMode)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/77ca4449-3bd3-4476-9502-6b05638ecf7f">Graphics::SetClip</a> method updates the clipping region of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to a region that is the combination of itself and the clipping region of another <b>Graphics</b> object.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c266648-77b7-486e-a2e0-b70e397bea01">SetClip(GraphicsPath*,CombineMode)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5c266648-77b7-486e-a2e0-b70e397bea01">Graphics::SetClip</a> method updates the clipping region of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to a region that is the combination of itself and the region specified by a graphics path. If a figure in the path is not closed, this method treats the nonclosed figure as if it were closed by a straight line that connects the figure's starting and ending points.

</td>
</tr>
</table>

## -parameters

