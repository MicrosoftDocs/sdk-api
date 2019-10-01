---
UID: NF:gdiplusimageattributes.ImageAttributes.SetWrapMode
title: ImageAttributes::SetWrapMode (gdiplusimageattributes.h)
author: windows-sdk-content
description: The ImageAttributes::SetWrapMode method sets the wrap mode of this ImageAttributes object.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetWrapMode_wrap_color_clamp_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setwrapmode.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImageAttributes class [GDI+],SetWrapMode method, ImageAttributes.SetWrapMode, ImageAttributes::SetWrapMode, SetWrapMode, SetWrapMode method [GDI+], SetWrapMode method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetWrapMode_wrap_color_clamp_, gdiplus._gdiplus_CLASS_ImageAttributes_SetWrapMode_wrap_color_clamp_
ms.topic: method
f1_keywords: 
 - "gdiplusimageattributes/ImageAttributes.SetWrapMode"
req.header: gdiplusimageattributes.h
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
 - ImageAttributes.SetWrapMode
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# ImageAttributes::SetWrapMode


## -description


The <b>ImageAttributes::SetWrapMode</b> method sets the wrap mode of this 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object.


## -parameters




### -param wrap [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a></b>

Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area. 


### -param color [in, ref, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color of pixels outside of a rendered image. This color is visible if the <i>wrap</i> parameter is set to <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapModeClamp</a> and the source rectangle passed to <a href="https://docs.microsoft.com/previous-versions/ms536037(v=vs.85)">DrawImage</a> is larger than the image itself. The default value is Color(), which is a <b>Color</b> object initialized to black. 


### -param clamp [in, optional]

Type: <b>BOOL</b>

This parameter has no effect in GDI+ version 1.0. Set this parameter to <b>FALSE</b>. The default value is <b>FALSE</b>. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-recoloring-use">Recoloring</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-wrapmode">WrapMode</a>
 

 

