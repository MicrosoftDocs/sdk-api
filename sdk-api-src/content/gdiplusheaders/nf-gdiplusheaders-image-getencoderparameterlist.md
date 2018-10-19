---
UID: NF:gdiplusheaders.Image.GetEncoderParameterList
title: Image::GetEncoderParameterList
author: windows-sdk-content
description: The Image::GetEncoderParameterList method gets a list of the parameters supported by a specified image encoder.
old-location: gdiplus\_gdiplus_CLASS_Image_GetEncoderParameterList_clsidEncoder_size_buffer_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getencoderparameterlist.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetEncoderParameterList, GetEncoderParameterList method [GDI+], GetEncoderParameterList method [GDI+],Image class, Image class [GDI+],GetEncoderParameterList method, Image.GetEncoderParameterList, Image::GetEncoderParameterList, _gdiplus_CLASS_Image_GetEncoderParameterList_clsidEncoder_size_buffer_, gdiplus._gdiplus_CLASS_Image_GetEncoderParameterList_clsidEncoder_size_buffer_
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
 - Image.GetEncoderParameterList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::GetEncoderParameterList


## -description


The <b>Image::GetEncoderParameterList</b> method gets a list of the parameters supported by a specified image encoder.


## -parameters




### -param clsidEncoder [in]

Type: <b>const CLSID*</b>

Pointer to a 
					<b>CLSID</b> that specifies the encoder. 


### -param size [in]

Type: <b>UINT</b>

Integer that specifies the size, in bytes, of the 
					<i>buffer</i> array. Call the <a href="https://msdn.microsoft.com/f7b0f80c-8fff-4fb7-bd7d-0b82275bd92d">Image::GetEncoderParameterListSize</a> method to obtain the required size. 


### -param buffer [out]

Type: <b><a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a>*</b>

Pointer to an 
					<a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a> object that receives the list of supported parameters. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The <b>Image::GetEncoderParameterList</b> method returns an array of 
				<a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a> objects. Before you call <b>Image::GetEncoderParameterList</b>, you must allocate a buffer large enough to receive that array, which is part of an 
				<a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a> object. You can call the <a href="https://msdn.microsoft.com/f7b0f80c-8fff-4fb7-bd7d-0b82275bd92d">Image::GetEncoderParameterListSize</a> method to get the size, in bytes, of the required 
				<b>EncoderParameters</b> object. 




## -see-also




<a href="https://msdn.microsoft.com/454d35be-ccb6-4a91-ba12-b07d55526f8e">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/b017e3d1-2faa-4d79-b1d8-8775b7be2dad">GetImageEncodersSize</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/f7b0f80c-8fff-4fb7-bd7d-0b82275bd92d">Image::GetEncoderParameterListSize</a>



<a href="https://msdn.microsoft.com/f9a5b4b1-4e25-42c8-a96b-a3104841e5f3">Using Image Encoders and Decoders</a>
 

 

