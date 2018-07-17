---
UID: NF:gdiplusbrush.LinearGradientBrush.GetWrapMode
title: LinearGradientBrush::GetWrapMode
author: windows-sdk-content
description: The LinearGradientBrush::GetWrapMode method gets the wrap mode for this brush. The wrap mode determines how an area is tiled when it is painted with a brush.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_GetWrapMode_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\getwrapmode.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetWrapMode, GetWrapMode method [GDI+], GetWrapMode method [GDI+],LinearGradientBrush class, LinearGradientBrush class [GDI+],GetWrapMode method, LinearGradientBrush.GetWrapMode, LinearGradientBrush::GetWrapMode, _gdiplus_CLASS_LinearGradientBrush_GetWrapMode_, gdiplus._gdiplus_CLASS_LinearGradientBrush_GetWrapMode_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KnownGamingPrivileges
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - LinearGradientBrush.GetWrapMode
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::GetWrapMode


## -description


The <b>LinearGradientBrush::GetWrapMode</b> method gets the wrap mode for this brush. The wrap mode determines how an area is tiled when it is painted with a brush. 


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a></b>
</strong>

This method returns one of the following elements of the <a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a> enumeration:

<ul>
<li>WrapModeTile</li>
<li>WrapModeTileFlipX</li>
<li>WrapModeTileFlipY</li>
<li>WrapModeTileFlipXY</li>
</ul>



## -remarks



The boundary lines of a linear gradient brush form a tile. When you paint an area with a linear gradient brush, the tile repeats. A linear gradient brush can have alternate tiles flipped in a certain direction, as specified by the wrap mode. Flipping has the effect of reversing the order of the colors.

The default wrap mode for a linear gradient brush is WrapModeTile, which indicates that no flipping occurs.


#### Examples



The following example creates a linear gradient brush and sets its wrap mode. Next, the code gets the brush's wrap mode and performs tasks based on the brush's current wrap mode.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetWrapMode(HDC hdc)
{
   Graphics myGraphics(hdc);

   // Create a linear gradient brush, and set its wrap mode.
   LinearGradientBrush linGrBrush( 
      Point(0,0),
      Point(200, 0),
      Color(255, 255, 0, 0),   // red
      Color(255, 0, 0, 255));  // blue

   linGrBrush.SetWrapMode(WrapModeTileFlipX);

   // Obtain information about the linear gradient brush.
   WrapMode wrapMode;
   wrapMode = linGrBrush.GetWrapMode();

   if (wrapMode == WrapModeTileFlipX)
   {
       // Do some task. 
   }
   else if (wrapMode == WrapModeTileFlipY)
   {
       // Do a different task.
   }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/e37b4c3a-b753-483a-990f-da3bcc70acf5">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/10b9aeb8-1925-4e59-8054-923b086af06f">LinearGradientBrush::SetWrapMode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a>



<a href="https://msdn.microsoft.com/c92aa519-647a-4cd9-b88e-b79be0116d05">Tiling a Shape with an Image</a>



<a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a>
 

 

