---
UID: NF:gdiplusheaders.Bitmap.GetHICON
title: Bitmap::GetHICON (gdiplusheaders.h)
description: The Bitmap::GetHICON method creates an icon from this Bitmap object.
helpviewer_keywords: ["Bitmap class [GDI+]","GetHICON method","Bitmap.GetHICON","Bitmap::GetHICON","GetHICON","GetHICON method [GDI+]","GetHICON method [GDI+]","Bitmap class","_gdiplus_CLASS_Bitmap_GetHICON_hicon_","gdiplus._gdiplus_CLASS_Bitmap_GetHICON_hicon_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_GetHICON_hicon_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\gethicon.htm
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],GetHICON method, Bitmap.GetHICON, Bitmap::GetHICON, GetHICON, GetHICON method [GDI+], GetHICON method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_GetHICON_hicon_, gdiplus._gdiplus_CLASS_Bitmap_GetHICON_hicon_
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
 - Bitmap::GetHICON
 - gdiplusheaders/Bitmap::GetHICON
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
 - Bitmap.GetHICON
---

# Bitmap::GetHICON


## -description

The <b>Bitmap::GetHICON</b> method creates an icon from this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object.

## -parameters

### -param hicon [out]

Type: <b>HICON*</b>

Pointer to an <b>HICON</b> that receives a handle to the icon.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>