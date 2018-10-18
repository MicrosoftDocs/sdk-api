---
UID: NF:gdiplusbrush.LinearGradientBrush.GetWrapMode
title: LinearGradientBrush::GetWrapMode
author: windows-sdk-content
description: The LinearGradientBrush::GetWrapMode method gets the wrap mode for this brush. The wrap mode determines how an area is tiled when it is painted with a brush.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_GetWrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\getwrapmode.htm
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetWrapMode, GetWrapMode method [GDI+], GetWrapMode method [GDI+],LinearGradientBrush class, LinearGradientBrush class [GDI+],GetWrapMode method, LinearGradientBrush.GetWrapMode, LinearGradientBrush::GetWrapMode, _gdiplus_CLASS_LinearGradientBrush_GetWrapMode_, gdiplus._gdiplus_CLASS_LinearGradientBrush_GetWrapMode_
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
 - LinearGradientBrush.GetWrapMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::GetWrapMode


## -description


The <b>LinearGradientBrush::GetWrapMode</b> method gets the wrap mode for this brush. The wrap mode determines how an area is tiled when it is painted with a brush. 


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a></b>
</strong>

This method returns one of the following elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a> enumeration:

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


```cpp
VOID Example_GetWrapMode(HDC hdc)
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
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533806(v=VS.85).aspx">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535349(v=VS.85).aspx">LinearGradientBrush::SetWrapMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533861(v=VS.85).aspx">Tiling a Shape with an Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a>
 

 

