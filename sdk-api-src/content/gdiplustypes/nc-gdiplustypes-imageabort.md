---
UID: NC:gdiplustypes.ImageAbort
title: ImageAbort
ms.date: 11/4/2019
ms.topic: language-reference
targetos: Windows
description: **ImageAbort** is the signature of a callback function that you implement in your application. During the process of creating or retrieving a thumbnail image, or drawing an image, GDI+ calls this function to give you the opportunity to abort the process.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplustypes.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - gdiplustypes.h
api_name:
 - ImageAbort
f1_keywords:
 - gdiplustypes/ImageAbort
dev_langs:
 - c++
---

## -description

**ImageAbort** is the signature of a callback function that you implement in your application. During the process of creating or retrieving a thumbnail image, or drawing an image, GDI+ calls this function to give you the opportunity to abort the process.

Examples of the callback function in use are the corresponding parameters of the [Image::GetThumbnailImage method](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-getthumbnailimage), and the [Graphics::DrawImage method](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint_inreal_inreal_inreal_inreal_inunit_inconstimageattributes_indrawimageabort_invoid)).

## -parameters

### -param Arg1

Type: **[VOID](/windows/win32/winprog/windows-data-types)\***

The callback data.

## -returns

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

Return **TRUE** to abort; otherwise **FALSE**.

## -remarks

## -see-also

[Image::GetThumbnailImage method](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-getthumbnailimage)

[Graphics::DrawImage method](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint_inreal_inreal_inreal_inreal_inunit_inconstimageattributes_indrawimageabort_invoid))