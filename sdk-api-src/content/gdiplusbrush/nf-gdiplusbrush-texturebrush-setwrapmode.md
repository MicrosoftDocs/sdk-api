---
UID: NF:gdiplusbrush.TextureBrush.SetWrapMode
title: TextureBrush::SetWrapMode (gdiplusbrush.h)
description: The TextureBrush::SetWrapMode method sets the wrap mode of this texture brush.
helpviewer_keywords: ["SetWrapMode","SetWrapMode method [GDI+]","SetWrapMode method [GDI+]","TextureBrush class","TextureBrush class [GDI+]","SetWrapMode method","TextureBrush.SetWrapMode","TextureBrush::SetWrapMode","_gdiplus_CLASS_TextureBrush_SetWrapMode_wrapMode_","gdiplus._gdiplus_CLASS_TextureBrush_SetWrapMode_wrapMode_"]
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_SetWrapMode_wrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\setwrapmode_88wrapmode.htm
ms.date: 12/05/2018
ms.keywords: SetWrapMode, SetWrapMode method [GDI+], SetWrapMode method [GDI+],TextureBrush class, TextureBrush class [GDI+],SetWrapMode method, TextureBrush.SetWrapMode, TextureBrush::SetWrapMode, _gdiplus_CLASS_TextureBrush_SetWrapMode_wrapMode_, gdiplus._gdiplus_CLASS_TextureBrush_SetWrapMode_wrapMode_
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
 - TextureBrush::SetWrapMode
 - gdiplusbrush/TextureBrush::SetWrapMode
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
 - TextureBrush.SetWrapMode
---

# TextureBrush::SetWrapMode


## -description

The <b>TextureBrush::SetWrapMode</b> method sets the wrap mode of this texture brush.

## -parameters

### -param wrapMode [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area when it is painted with this texture brush.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

An area that extends beyond the boundaries of the brush is tiled with repeated copies of the brush. A texture brush may have alternate tiles flipped in a certain direction, as specified by the wrap mode. Flipping has the effect of reversing the brush's image. For example, if the wrap mode is specified as <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">WrapModeTileFlipX</a>, the brush is flipped about a line that is parallel to the y-axis.

The texture brush is always oriented at (0, 0). If the wrap mode is specified as <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">WrapModeClamp</a>, no area outside of the brush is tiled. For example, suppose you create a texture brush, specifying <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">WrapModeClamp</a> as the wrap mode:

<code>TextureBrush(&amp;SomeImage, WrapModeClamp)</code>

Then you paint an area with the brush. If the size of the brush has a height of 50 and the painted area is a rectangle with its upper-left corner at (0, 50), you will see no repeated copies of the brush (no tiling).

The default wrap mode for a texture brush is <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">WrapModeTile</a>, which specifies no flipping of the tile and no clamping.


#### Examples

The following example creates a texture brush, sets the wrap mode of the brush, and uses the brush to fill a rectangle.


```cpp
VOID Example_SetWrapMode(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"HouseAndTree.gif");
   TextureBrush textureBrush(&image);
   textureBrush.SetWrapMode(WrapModeTileFlipX);
   graphics.FillRectangle(&textureBrush, 0, 0, 400, 200);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-an-image-texture-use">Filling a Shape with an Image Texture</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nf-gdiplusbrush-texturebrush-getwrapmode">TextureBrush::GetWrapMode</a>



<a href="/windows/desktop/gdiplus/-gdiplus-tiling-a-shape-with-an-image-use">Tiling a Shape with an Image</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a>