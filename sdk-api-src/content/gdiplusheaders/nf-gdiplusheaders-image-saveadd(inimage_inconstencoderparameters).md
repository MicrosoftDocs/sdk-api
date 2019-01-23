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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>*</b>

Pointer to an 
					<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object that holds the frame to be added. 


### -param encoderParams [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534435(v=VS.85).aspx">EncoderParameters</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms534435(v=VS.85).aspx">EncoderParameters</a> object that contains parameters required by the image encoder used in the save-add operation. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534434(v=VS.85).aspx">EncoderParameter</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534435(v=VS.85).aspx">EncoderParameters</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534080(v=VS.85).aspx">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535399(v=VS.85).aspx">Image::Save Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535398(v=VS.85).aspx">Image::SaveAdd Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535402(v=VS.85).aspx">Image::SelectActiveFrame</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533814(v=VS.85).aspx">Using Image Encoders and Decoders</a>
 

 

