---
UID: NF:gdiplusheaders.Image.SaveAdd(Image,constEncoderParameters)
title: Image::SaveAdd(IN Image,IN const EncoderParameters) (gdiplusheaders.h)
description: The Image::SaveAdd method adds a frame to a file or stream specified in a previous call to the Save method. (overload 2/2)
helpviewer_keywords: ["Image class [GDI+]","SaveAdd method","Image.SaveAdd","Image.SaveAdd(IN Image","IN const EncoderParameters)","Image.SaveAdd(Image*","const EncoderParameters*)","Image::SaveAdd","Image::SaveAdd(IN Image","IN const EncoderParameters)","SaveAdd","SaveAdd method [GDI+]","SaveAdd method [GDI+]","Image class","_gdiplus_CLASS_Image_SaveAdd_newImage_encoderParams_","gdiplus._gdiplus_CLASS_Image_SaveAdd_newImage_encoderParams_"]
old-location: gdiplus\_gdiplus_CLASS_Image_SaveAdd_newImage_encoderParams_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\imagesaveaddmethods\saveadd_17newimage_encoderparams.htm
ms.date: 12/05/2018
ms.keywords: Image class [GDI+],SaveAdd method, Image.SaveAdd, Image.SaveAdd(IN Image,IN const EncoderParameters), Image.SaveAdd(Image*,const EncoderParameters*), Image::SaveAdd, Image::SaveAdd(IN Image,IN const EncoderParameters), SaveAdd, SaveAdd method [GDI+], SaveAdd method [GDI+],Image class, _gdiplus_CLASS_Image_SaveAdd_newImage_encoderParams_, gdiplus._gdiplus_CLASS_Image_SaveAdd_newImage_encoderParams_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Image::SaveAdd
 - gdiplusheaders/Image::SaveAdd
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
 - Image.SaveAdd
---

# Image::SaveAdd(IN Image,IN const EncoderParameters)


## -description

The <b>Image::SaveAdd</b> method adds a frame to a file or stream specified in a previous call to the 
			<b>Save</b> method.

## -parameters

### -param newImage [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

Pointer to an 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object that holds the frame to be added.

### -param encoderParams [in]

Type: <b>const <a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a>*</b>

Pointer to an <a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a> object that contains parameters required by the image encoder used in the save-add operation.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/previous-versions/ms534434(v=vs.85)">EncoderParameter</a>



<a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a>



<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)">Image::Save Methods</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)">Image::SaveAdd Methods</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe">Image::SelectActiveFrame</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>
