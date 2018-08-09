---
UID: NF:gdiplusbrush.TextureBrush.SetWrapMode
title: TextureBrush::SetWrapMode
author: windows-sdk-content
description: The TextureBrush::SetWrapMode method sets the wrap mode of this texture brush.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_SetWrapMode_wrapMode_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\setwrapmode_88wrapmode.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SetWrapMode, SetWrapMode method [GDI+], SetWrapMode method [GDI+],TextureBrush class, TextureBrush class [GDI+],SetWrapMode method, TextureBrush.SetWrapMode, TextureBrush::SetWrapMode, _gdiplus_CLASS_TextureBrush_SetWrapMode_wrapMode_, gdiplus._gdiplus_CLASS_TextureBrush_SetWrapMode_wrapMode_
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
 - TextureBrush.SetWrapMode
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# TextureBrush::SetWrapMode


## -description


The <b>TextureBrush::SetWrapMode</b> method sets the wrap mode of this texture brush.


## -parameters




### -param wrapMode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area when it is painted with this texture brush. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



An area that extends beyond the boundaries of the brush is tiled with repeated copies of the brush. A texture brush may have alternate tiles flipped in a certain direction, as specified by the wrap mode. Flipping has the effect of reversing the brush's image. For example, if the wrap mode is specified as <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">WrapModeTileFlipX</a>, the brush is flipped about a line that is parallel to the y-axis.

The texture brush is always oriented at (0, 0). If the wrap mode is specified as <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">WrapModeClamp</a>, no area outside of the brush is tiled. For example, suppose you create a texture brush, specifying <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">WrapModeClamp</a> as the wrap mode:

<code>TextureBrush(&amp;SomeImage, WrapModeClamp)</code>

Then you paint an area with the brush. If the size of the brush has a height of 50 and the painted area is a rectangle with its upper-left corner at (0, 50), you will see no repeated copies of the brush (no tiling).

The default wrap mode for a texture brush is <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">WrapModeTile</a>, which specifies no flipping of the tile and no clamping.


#### Examples

The following example creates a texture brush, sets the wrap mode of the brush, and uses the brush to fill a rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetWrapMode(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"HouseAndTree.gif");
   TextureBrush textureBrush(&amp;image);
   textureBrush.SetWrapMode(WrapModeTileFlipX);
   graphics.FillRectangle(&amp;textureBrush, 0, 0, 400, 200);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533858(v=VS.85).aspx">Filling a Shape with an Image Texture</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534527(v=VS.85).aspx">TextureBrush::GetWrapMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533861(v=VS.85).aspx">Tiling a Shape with an Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a>
 

 

