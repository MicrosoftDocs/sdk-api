---
UID: NF:gdipluspath.PathGradientBrush.SetWrapMode
title: PathGradientBrush::SetWrapMode
author: windows-sdk-content
description: The PathGradientBrush::SetWrapMode method sets the wrap mode of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetWrapMode_wrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setwrapmode_12wrapmode.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PathGradientBrush class [GDI+],SetWrapMode method, PathGradientBrush.SetWrapMode, PathGradientBrush::SetWrapMode, SetWrapMode, SetWrapMode method [GDI+], SetWrapMode method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetWrapMode_wrapMode_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetWrapMode_wrapMode_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspath.h
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
 - PathGradientBrush.SetWrapMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::SetWrapMode


## -description


The <b>PathGradientBrush::SetWrapMode</b> method sets the wrap mode of this path gradient brush.


## -parameters




### -param wrapMode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a> enumeration that specifies how areas painted with the path gradient brush will be tiled. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapModeClamp</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



The bounding rectangle of a path gradient brush is the smallest rectangle that encloses the brush's boundary path. When you paint the bounding rectangle with the path gradient brush, only the area inside the boundary path gets filled. The area inside the bounding rectangle but outside the boundary path does not get filled.


<a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapModeClamp</a> (the default wrap mode) indicates that no painting occurs outside of the brush's bounding rectangle. All of the other wrap modes indicate that areas outside the brush's bounding rectangle will be tiled. Each tile is a copy (possibly flipped) of the filled path inside its bounding rectangle.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>object based on a triangular path. The code calls the <b>PathGradientBrush::SetWrapMode</b> method of the 
						<b>PathGradientBrush</b>object to set the brush's wrap mode to <a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapModeTileFlipX</a>. The 
						<a href="https://msdn.microsoft.com/en-us/library/ms535773(v=VS.85).aspx">Graphics::FillRectangle</a> method uses the path gradient brush to tile a large area. 

The output of the code is a grid of tiles. As you move from one tile to the next in a given row, the image (filled boundary path inside the bounding rectangle) is flipped horizontally.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetWrapMode(HDC hdc)
{
   Graphics graphics(hdc);

   Point points[] = {
      Point(0, 0), 
      Point(100, 0), 
      Point(100, 100)};

   Color colors[] = {
      Color(255, 255, 0, 0),   // red
      Color(255, 0, 0, 255),   // blue
      Color(255, 0, 255, 0)};  // green

   INT count = 3;

   PathGradientBrush pthGrBrush(points, 3);
   pthGrBrush.SetSurroundColors(colors, &amp;count);
   pthGrBrush.SetWrapMode(WrapModeTileFlipX);

   graphics.FillRectangle(&amp;pthGrBrush, 0, 0, 800, 800); 
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535074(v=VS.85).aspx">PathGradientBrush::GetWrapMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535092(v=VS.85).aspx">PathGradientBrush::SetWrapMode</a>
 

 

