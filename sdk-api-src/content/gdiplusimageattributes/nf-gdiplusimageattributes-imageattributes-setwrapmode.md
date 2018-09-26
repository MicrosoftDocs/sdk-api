---
UID: NF:gdiplusimageattributes.ImageAttributes.SetWrapMode
title: ImageAttributes::SetWrapMode
author: windows-sdk-content
description: The ImageAttributes::SetWrapMode method sets the wrap mode of this ImageAttributes object.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetWrapMode_wrap_color_clamp_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setwrapmode.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: ImageAttributes class [GDI+],SetWrapMode method, ImageAttributes.SetWrapMode, ImageAttributes::SetWrapMode, SetWrapMode, SetWrapMode method [GDI+], SetWrapMode method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetWrapMode_wrap_color_clamp_, gdiplus._gdiplus_CLASS_ImageAttributes_SetWrapMode_wrap_color_clamp_
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetWrapMode


## -description


The <b>ImageAttributes::SetWrapMode</b> method sets the wrap mode of this 
			<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object.


## -parameters




### -param wrap [in]

Type: <b><a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a></b>

Element of the <a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area. 


### -param color [in, ref, optional]

Type: <b>const <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object that specifies the color of pixels outside of a rendered image. This color is visible if the <i>wrap</i> parameter is set to <a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapModeClamp</a> and the source rectangle passed to <a href="https://msdn.microsoft.com/ec2eb9c8-e5f1-4f0d-968f-e4ac16d670d6">DrawImage</a> is larger than the image itself. The default value is Color(), which is a <b>Color</b> object initialized to black. 


### -param clamp [in, optional]

Type: <b>BOOL</b>

This parameter has no effect in GDI+ version 1.0. Set this parameter to <b>FALSE</b>. The default value is <b>FALSE</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/7e018c5a-7933-43b6-b7b3-ee9daea16eb9">Recoloring</a>



<a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a>
 

 

