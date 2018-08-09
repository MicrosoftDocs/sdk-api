---
UID: NF:gdiplusimageattributes.ImageAttributes.SetWrapMode
title: ImageAttributes::SetWrapMode
author: windows-sdk-content
description: The ImageAttributes::SetWrapMode method sets the wrap mode of this ImageAttributes object.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetWrapMode_wrap_color_clamp_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setwrapmode.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ImageAttributes class [GDI+],SetWrapMode method, ImageAttributes.SetWrapMode, ImageAttributes::SetWrapMode, SetWrapMode, SetWrapMode method [GDI+], SetWrapMode method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetWrapMode_wrap_color_clamp_, gdiplus._gdiplus_CLASS_ImageAttributes_SetWrapMode_wrap_color_clamp_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - ImageAttributes.SetWrapMode
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetWrapMode


## -description


The <b>ImageAttributes::SetWrapMode</b> method sets the wrap mode of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object.


## -parameters




### -param wrap [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area. 


### -param color [in, ref, optional]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object that specifies the color of pixels outside of a rendered image. This color is visible if the <i>wrap</i> parameter is set to <a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapModeClamp</a> and the source rectangle passed to <a href="https://msdn.microsoft.com/en-us/library/ms536037(v=VS.85).aspx">DrawImage</a> is larger than the image itself. The default value is Color(), which is a <b>Color</b> object initialized to black. 


### -param clamp [in, optional]

Type: <b>BOOL</b>

This parameter has no effect in GDI+ version 1.0. Set this parameter to <b>FALSE</b>. The default value is <b>FALSE</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533809(v=VS.85).aspx">Recoloring</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a>
 

 

