---
UID: NF:gdiplusheaders.Image.GetEncoderParameterList
title: Image::GetEncoderParameterList
author: windows-sdk-content
description: The Image::GetEncoderParameterList method gets a list of the parameters supported by a specified image encoder.
old-location: gdiplus\_gdiplus_CLASS_Image_GetEncoderParameterList_clsidEncoder_size_buffer_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getencoderparameterlist.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
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
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Image.GetEncoderParameterList
: 
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
					<i>buffer</i> array. Call the <a href="https://msdn.microsoft.com/en-us/library/ms535375(v=VS.85).aspx">Image::GetEncoderParameterListSize</a> method to obtain the required size. 


### -param buffer [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534435(v=VS.85).aspx">EncoderParameters</a>*</b>

Pointer to an 
					<a href="https://msdn.microsoft.com/en-us/library/ms534435(v=VS.85).aspx">EncoderParameters</a> object that receives the list of supported parameters. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



The <b>Image::GetEncoderParameterList</b> method returns an array of 
				<a href="https://msdn.microsoft.com/en-us/library/ms534434(v=VS.85).aspx">EncoderParameter</a> objects. Before you call <b>Image::GetEncoderParameterList</b>, you must allocate a buffer large enough to receive that array, which is part of an 
				<a href="https://msdn.microsoft.com/en-us/library/ms534435(v=VS.85).aspx">EncoderParameters</a> object. You can call the <a href="https://msdn.microsoft.com/en-us/library/ms535375(v=VS.85).aspx">Image::GetEncoderParameterListSize</a> method to get the size, in bytes, of the required 
				<b>EncoderParameters</b> object. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534080(v=VS.85).aspx">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534081(v=VS.85).aspx">GetImageEncodersSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535375(v=VS.85).aspx">Image::GetEncoderParameterListSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533814(v=VS.85).aspx">Using Image Encoders and Decoders</a>
 

 

