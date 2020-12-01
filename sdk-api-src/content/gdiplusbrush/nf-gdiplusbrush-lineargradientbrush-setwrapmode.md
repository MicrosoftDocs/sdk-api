---
UID: NF:gdiplusbrush.LinearGradientBrush.SetWrapMode
title: LinearGradientBrush::SetWrapMode (gdiplusbrush.h)
description: The LinearGradientBrush::SetWrapMode method sets the wrap mode of this linear gradient brush.
helpviewer_keywords: ["LinearGradientBrush class [GDI+]","SetWrapMode method","LinearGradientBrush.SetWrapMode","LinearGradientBrush::SetWrapMode","SetWrapMode","SetWrapMode method [GDI+]","SetWrapMode method [GDI+]","LinearGradientBrush class","_gdiplus_CLASS_LinearGradientBrush_SetWrapMode_wrapMode_","gdiplus._gdiplus_CLASS_LinearGradientBrush_SetWrapMode_wrapMode_"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetWrapMode_wrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\setwrapmode_76wrapmode.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush class [GDI+],SetWrapMode method, LinearGradientBrush.SetWrapMode, LinearGradientBrush::SetWrapMode, SetWrapMode, SetWrapMode method [GDI+], SetWrapMode method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetWrapMode_wrapMode_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetWrapMode_wrapMode_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - LinearGradientBrush::SetWrapMode
 - gdiplusbrush/LinearGradientBrush::SetWrapMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - LinearGradientBrush.SetWrapMode
---

# LinearGradientBrush::SetWrapMode


## -description

The <b>LinearGradientBrush::SetWrapMode</b> method sets the wrap mode of this linear gradient brush.

## -parameters

### -param wrapMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a> enumeration that specifies how areas painted with this linear gradient brush will be tiled. The value of this parameter must be one of the following elements: 


<ul>
<li>WrapModeTile</li>
<li>WrapModeTileFlipX</li>
<li>WrapModeTileFlipY</li>
<li>WrapModeTileFlipXY</li>
</ul>

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The boundary lines of a linear gradient brush form a tile. When you paint an area with a linear gradient brush, the tile repeats. A linear gradient brush may have alternate tiles flipped in a certain direction, as specified by the wrap mode. Flipping has the effect of reversing the order of the colors.

The wrap mode defaults to WrapModeTile when a 
				<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a> object is constructed. 


#### Examples



The following example creates a linear gradient brush and uses it to fill a rectangle. Next, the code modifies the brush's wrap mode and uses the modified brush to fill another rectangle.


```cpp
VOID Example_SetWrapMode(HDC hdc)
{
   Graphics myGraphics(hdc);

   LinearGradientBrush linGrBrush( 
      Rect(0, 0, 100, 50),
      Color(255, 255, 0, 0),  // red
      Color(255, 0, 0, 255),  // blue
      LinearGradientModeHorizontal);

   // Fill a large area using the gradient brush with the default wrap mode.
   myGraphics.FillRectangle(&linGrBrush, 0, 0, 800, 50);

   linGrBrush.SetWrapMode(WrapModeTileFlipX);

   // Fill a large area using the gradient brush with the new wrap mode.
   myGraphics.FillRectangle(&linGrBrush, 0, 75, 800, 50);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-linear-gradient-use">Creating a Linear Gradient</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-getwrapmode">LinearGradientBrush::GetWrapMode</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/gdiplus/-gdiplus-tiling-a-shape-with-an-image-use">Tiling a Shape with an Image</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a>