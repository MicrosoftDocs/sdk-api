---
UID: NF:gdiplusimagecodec.GetImageEncodersSize
title: GetImageEncodersSize function (gdiplusimagecodec.h)

description: The GetImageEncodersSize function gets the number of available image encoders and the total size of the array of ImageCodecInfo objects that is returned by the GetImageEncoders function.
old-location: gdiplus\_gdiplus_FUNC_GetImageEncodersSize_numEncoders_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\getimageencoderssize.htm

ms.date: 12/05/2018
ms.keywords: GetImageEncodersSize, GetImageEncodersSize function [GDI+], _gdiplus_FUNC_GetImageEncodersSize_numEncoders_size_, gdiplus._gdiplus_FUNC_GetImageEncodersSize_numEncoders_size_, gdiplusimagecodec/GetImageEncodersSize
ms.topic: function
f1_keywords: 
 - "gdiplusimagecodec/GetImageEncodersSize"
dev_langs:
 - c++
req.header: gdiplusimagecodec.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - GetImageEncodersSize
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# GetImageEncodersSize function


## -description


The <b>GetImageEncodersSize</b> function gets the number of available image encoders and the total size of the array of 
			<a href="https://docs.microsoft.com/previous-versions/ms534466(v=vs.85)">ImageCodecInfo</a> objects that is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a> function.


## -parameters




### -param numEncoders [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the number of available image encoders. 


### -param size [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the total size, in bytes, of the array of 
					<a href="https://docs.microsoft.com/previous-versions/ms534466(v=vs.85)">ImageCodecInfo</a> objects that is returned by <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a>. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the function succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the function fails, it returns one of the other elements of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders">GetImageDecoders</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize">GetImageDecodersSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>
 

 

