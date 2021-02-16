---
UID: NF:gdiplusheaders.Image.SelectActiveFrame
title: Image::SelectActiveFrame (gdiplusheaders.h)
description: The Image::SelectActiveFrame method selects the frame in this Image object specified by a dimension and an index.
helpviewer_keywords: ["Image class [GDI+]","SelectActiveFrame method","Image.SelectActiveFrame","Image::SelectActiveFrame","SelectActiveFrame","SelectActiveFrame method [GDI+]","SelectActiveFrame method [GDI+]","Image class","_gdiplus_CLASS_Image_SelectActiveFrame_dimensionID_frameIndex_","gdiplus._gdiplus_CLASS_Image_SelectActiveFrame_dimensionID_frameIndex_"]
old-location: gdiplus\_gdiplus_CLASS_Image_SelectActiveFrame_dimensionID_frameIndex_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\selectactiveframe.htm
ms.date: 12/05/2018
ms.keywords: Image class [GDI+],SelectActiveFrame method, Image.SelectActiveFrame, Image::SelectActiveFrame, SelectActiveFrame, SelectActiveFrame method [GDI+], SelectActiveFrame method [GDI+],Image class, _gdiplus_CLASS_Image_SelectActiveFrame_dimensionID_frameIndex_, gdiplus._gdiplus_CLASS_Image_SelectActiveFrame_dimensionID_frameIndex_
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
 - Image::SelectActiveFrame
 - gdiplusheaders/Image::SelectActiveFrame
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
 - Image.SelectActiveFrame
---

# Image::SelectActiveFrame


## -description

The <b>Image::SelectActiveFrame</b> method selects the frame in this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object specified by a dimension and an index.

## -parameters

### -param dimensionID [in]

Type: <b>const GUID*</b>

Pointer to a 
					<b>GUID</b> that specifies the frame dimension. 
					<b>GUID</b>s that identify various frame dimensions are defined in Gdiplusimaging.h.

### -param frameIndex [in]

Type: <b>UINT</b>

Integer that specifies the index of the frame within the specified frame dimension.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

<b>Remarks</b>

When you call the <b>Image::SelectActiveFrame</b> method, all changes that you made to the previously active frame are discarded. If you want to retain changes that you make to a frame, call the 
						<b>Save</b> method before you switch to a different frame.

Among all the image formats currently supported by GDI+, the only formats that support multiple-frame images are GIF and TIFF. When you call the <b>Image::SelectActiveFrame</b> method on a GIF image, you should use FrameDimensionTime. When you call the <b>Image::SelectActiveFrame</b> method on a TIFF image, you should use FrameDimensionPage.

## -see-also

<a href="/previous-versions/ms534434(v=vs.85)">EncoderParameter</a>



<a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a>



<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)">Image::Save Methods</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)">Image::SaveAdd Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>