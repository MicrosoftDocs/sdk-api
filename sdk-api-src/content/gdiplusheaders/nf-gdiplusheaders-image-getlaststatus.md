---
UID: NF:gdiplusheaders.Image.GetLastStatus
title: Image::GetLastStatus (gdiplusheaders.h)
description: The Image::GetLastStatus method returns a value that indicates the nature of this Image object's most recent method failure.
helpviewer_keywords: ["GetLastStatus","GetLastStatus method [GDI+]","GetLastStatus method [GDI+]","Image class","Image class [GDI+]","GetLastStatus method","Image.GetLastStatus","Image::GetLastStatus","_gdiplus_CLASS_Image_GetLastStatus_","gdiplus._gdiplus_CLASS_Image_GetLastStatus_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getlaststatus_65.htm
ms.date: 12/05/2018
ms.keywords: GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],Image class, Image class [GDI+],GetLastStatus method, Image.GetLastStatus, Image::GetLastStatus, _gdiplus_CLASS_Image_GetLastStatus_, gdiplus._gdiplus_CLASS_Image_GetLastStatus_
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
 - Image::GetLastStatus
 - gdiplusheaders/Image::GetLastStatus
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
 - Image.GetLastStatus
---

# Image::GetLastStatus


## -description

The <b>Image::GetLastStatus</b> method returns a value that indicates the nature of this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object's most recent method failure.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

The <b>Image::GetLastStatus</b> method returns an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If no methods invoked on this 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object have failed since the previous call to <b>Image::GetLastStatus</b>, then <b>Image::GetLastStatus</b> returns Ok.

If at least one method invoked on this 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object has failed since the previous call to <b>Image::GetLastStatus</b>, then <b>Image::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.

## -remarks

You can call <b>Image::GetLastStatus</b> immediately after constructing an 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object to determine whether the constructor succeeded.

The first time you call the <b>Image::GetLastStatus</b> method of an 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the 
				<b>Image</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>
