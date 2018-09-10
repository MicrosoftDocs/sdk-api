---
UID: NF:gdiplusbrush.LinearGradientBrush.SetWrapMode
title: LinearGradientBrush::SetWrapMode
author: windows-sdk-content
description: The LinearGradientBrush::SetWrapMode method sets the wrap mode of this linear gradient brush.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetWrapMode_wrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\setwrapmode_76wrapmode.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: LinearGradientBrush class [GDI+],SetWrapMode method, LinearGradientBrush.SetWrapMode, LinearGradientBrush::SetWrapMode, SetWrapMode, SetWrapMode method [GDI+], SetWrapMode method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetWrapMode_wrapMode_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetWrapMode_wrapMode_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusbrush.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - LinearGradientBrush.SetWrapMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::SetWrapMode


## -description


The <b>LinearGradientBrush::SetWrapMode</b> method sets the wrap mode of this linear gradient brush.


## -parameters




### -param wrapMode [in]

Type: <b><a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a></b>

Element of the <a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a> enumeration that specifies how areas painted with this linear gradient brush will be tiled. The value of this parameter must be one of the following elements: 


<ul>
<li>WrapModeTile</li>
<li>WrapModeTileFlipX</li>
<li>WrapModeTileFlipY</li>
<li>WrapModeTileFlipXY</li>
</ul>

## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The boundary lines of a linear gradient brush form a tile. When you paint an area with a linear gradient brush, the tile repeats. A linear gradient brush may have alternate tiles flipped in a certain direction, as specified by the wrap mode. Flipping has the effect of reversing the order of the colors.

The wrap mode defaults to WrapModeTile when a 
				<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object is constructed. 


#### Examples



The following example creates a linear gradient brush and uses it to fill a rectangle. Next, the code modifies the brush's wrap mode and uses the modified brush to fill another rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetWrapMode(HDC hdc)
{
   Graphics myGraphics(hdc);

   LinearGradientBrush linGrBrush( 
      Rect(0, 0, 100, 50),
      Color(255, 255, 0, 0),  // red
      Color(255, 0, 0, 255),  // blue
      LinearGradientModeHorizontal);

   // Fill a large area using the gradient brush with the default wrap mode.
   myGraphics.FillRectangle(&amp;linGrBrush, 0, 0, 800, 50);

   linGrBrush.SetWrapMode(WrapModeTileFlipX);

   // Fill a large area using the gradient brush with the new wrap mode.
   myGraphics.FillRectangle(&amp;linGrBrush, 0, 75, 800, 50);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/9b0236b2-be6b-4918-a106-5b0e6c3dd5ff">Creating a Linear Gradient</a>



<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/149504d3-ca48-4fec-b090-33fb3f08b230">LinearGradientBrush::GetWrapMode</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/c92aa519-647a-4cd9-b88e-b79be0116d05">Tiling a Shape with an Image</a>



<a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a>
 

 

