---
UID: NF:gdiplusheaders.Image.GetEncoderParameterListSize
title: Image::GetEncoderParameterListSize
author: windows-sdk-content
description: The Image::GetEncoderParameterListSize method gets the size, in bytes, of the parameter list for a specified image encoder.
old-location: gdiplus\_gdiplus_CLASS_Image_GetEncoderParameterListSize_clsidEncoder_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getencoderparameterlistsize.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetEncoderParameterListSize, GetEncoderParameterListSize method [GDI+], GetEncoderParameterListSize method [GDI+],Image class, Image class [GDI+],GetEncoderParameterListSize method, Image.GetEncoderParameterListSize, Image::GetEncoderParameterListSize, _gdiplus_CLASS_Image_GetEncoderParameterListSize_clsidEncoder_, gdiplus._gdiplus_CLASS_Image_GetEncoderParameterListSize_clsidEncoder_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
 - Image.GetEncoderParameterListSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Image.GetEncoderParameterListSize
: 
req.product: GDI+ 1.0
---

# Image::GetEncoderParameterListSize


## -description


The <b>Image::GetEncoderParameterListSize</b> method gets the size, in bytes, of the parameter list for a specified image encoder.


## -parameters




### -param clsidEncoder [in]

Type: <b>const CLSID*</b>

Pointer to a 
					<b>CLSID</b> that specifies the encoder. 


## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

This method returns the size, in bytes, of the parameter list.




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/ms535374(v=VS.85).aspx">Image::GetEncoderParameterList</a> method returns an array of 
				<a href="https://msdn.microsoft.com/en-us/library/ms534434(v=VS.85).aspx">EncoderParameter</a> objects. Before you call <b>Image::GetEncoderParameterList</b>, you must allocate a buffer large enough to receive that array, which is part of an 
				<a href="https://msdn.microsoft.com/en-us/library/ms534435(v=VS.85).aspx">EncoderParameters</a> object. You can call the <b>Image::GetEncoderParameterListSize</b> method to get the size, in bytes, of the required 
				<b>EncoderParameters</b> object. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534080(v=VS.85).aspx">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534081(v=VS.85).aspx">GetImageEncodersSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535374(v=VS.85).aspx">Image::GetEncoderParameterList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533814(v=VS.85).aspx">Using Image Encoders and Decoders</a>
 

 

