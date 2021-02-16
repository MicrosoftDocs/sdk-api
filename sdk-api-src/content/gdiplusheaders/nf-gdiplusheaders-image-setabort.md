---
UID: NF:gdiplusheaders.Image.SetAbort
title: Image::SetAbort (gdiplusheaders.h)
description: The Image::SetAbort method sets the object whose Abort method is called periodically during time-consuming rendering operation.
helpviewer_keywords: ["Image class [GDI+]","SetAbort method","Image.SetAbort","Image::SetAbort","SetAbort","SetAbort method [GDI+]","SetAbort method [GDI+]","Image class","_gdiplus_CLASS_Image_SetAbort_","gdiplus._gdiplus_CLASS_Image_SetAbort_"]
old-location: gdiplus\_gdiplus_CLASS_Image_SetAbort_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\setabort.htm
ms.date: 12/05/2018
ms.keywords: Image class [GDI+],SetAbort method, Image.SetAbort, Image::SetAbort, SetAbort, SetAbort method [GDI+], SetAbort method [GDI+],Image class, _gdiplus_CLASS_Image_SetAbort_, gdiplus._gdiplus_CLASS_Image_SetAbort_
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - Image::SetAbort
 - gdiplusheaders/Image::SetAbort
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
 - Image.SetAbort
---

# Image::SetAbort


## -description

The <b>Image::SetAbort</b> method sets the object whose <b>Abort</b> method is called periodically during time-consuming rendering operation.

## -parameters

### -param pIAbort

Type: <b><a href="/windows/desktop/api/gdiplustypes/ns-gdiplustypes-gdiplusabort">GdiplusAbort</a>*</b>

Pointer to an application-defined descendant of the <a href="/windows/desktop/api/gdiplustypes/ns-gdiplustypes-gdiplusabort">GdiplusAbort</a> structure.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>