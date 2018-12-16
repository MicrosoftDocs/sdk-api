---
UID: NF:gdiplusheaders.Image.SaveAdd(IN Image,IN const EncoderParameters)
title: Image::SaveAdd(IN Image,IN const EncoderParameters)
author: windows-sdk-content
description: The Image::SaveAdd method adds a frame to a file or stream specified in a previous call to the Save method.
old-location: gdiplus\_gdiplus_CLASS_Image_SaveAdd_newImage_encoderParams_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\imagesaveaddmethods\saveadd_17newimage_encoderparams.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Image class [GDI+],SaveAdd method, Image.SaveAdd, Image.SaveAdd(IN Image,IN const EncoderParameters), Image.SaveAdd(Image*,const EncoderParameters*), Image::SaveAdd, Image::SaveAdd(IN Image,IN const EncoderParameters), SaveAdd, SaveAdd method [GDI+], SaveAdd method [GDI+],Image class, _gdiplus_CLASS_Image_SaveAdd_newImage_encoderParams_, gdiplus._gdiplus_CLASS_Image_SaveAdd_newImage_encoderParams_
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
 - Image.SaveAdd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::SaveAdd(IN Image,IN const EncoderParameters)


## -description


The <b>Image::SaveAdd</b> method adds a frame to a file or stream specified in a previous call to the 
			<b>Save</b> method.


## -parameters




### -param newImage [in]

Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>

Pointer to an 
					<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that holds the frame to be added. 


### -param encoderParams [in]

Type: <b>const <a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a> object that contains parameters required by the image encoder used in the save-add operation. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a>



<a href="https://msdn.microsoft.com/347275b5-22d2-47ad-9754-0bd213689bf0">EncoderParameters</a>



<a href="https://msdn.microsoft.com/454d35be-ccb6-4a91-ba12-b07d55526f8e">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ea264188-3c39-4f00-84f3-114c81a5642e">Image::Save Methods</a>



<a href="https://msdn.microsoft.com/e597f6e6-6e07-4afb-8905-26e4af961685">Image::SaveAdd Methods</a>



<a href="https://msdn.microsoft.com/b9d62f6d-253e-423e-9dba-6b55b1a8391a">Image::SelectActiveFrame</a>



<a href="https://msdn.microsoft.com/f9a5b4b1-4e25-42c8-a96b-a3104841e5f3">Using Image Encoders and Decoders</a>
 

 

