---
UID: NF:gdiplusheaders.Bitmap.Bitmap(constBITMAPINFO,VOID)
title: Bitmap::Bitmap(IN const BITMAPINFO,IN VOID) (gdiplusheaders.h)
description: Creates a Bitmap::Bitmap object based on a BITMAPINFO structure and an array of pixel data.
helpviewer_keywords: ["Bitmap","Bitmap class [GDI+]","Bitmap constructor","Bitmap constructor [GDI+]","Bitmap constructor [GDI+]","Bitmap class","Bitmap.Bitmap","Bitmap.Bitmap(IN const BITMAPINFO","IN VOID)","Bitmap.Bitmap(const BITMAPINFO*","VOID*)","Bitmap::Bitmap","Bitmap::Bitmap(IN const BITMAPINFO","IN VOID)","_gdiplus_CLASS_Bitmap_Bitmap_gdiBitmapInfo_gdiBitmapData_","gdiplus._gdiplus_CLASS_Bitmap_Bitmap_gdiBitmapInfo_gdiBitmapData_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Bitmap_gdiBitmapInfo_gdiBitmapData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapconstructors\bitmap_30gdibitmapinfo_gdibitmapdata.htm
ms.date: 12/05/2018
ms.keywords: Bitmap, Bitmap class [GDI+],Bitmap constructor, Bitmap constructor [GDI+], Bitmap constructor [GDI+],Bitmap class, Bitmap.Bitmap, Bitmap.Bitmap(IN const BITMAPINFO,IN VOID), Bitmap.Bitmap(const BITMAPINFO*,VOID*), Bitmap::Bitmap, Bitmap::Bitmap(IN const BITMAPINFO,IN VOID), _gdiplus_CLASS_Bitmap_Bitmap_gdiBitmapInfo_gdiBitmapData_, gdiplus._gdiplus_CLASS_Bitmap_Bitmap_gdiBitmapInfo_gdiBitmapData_
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
 - Bitmap::Bitmap
 - gdiplusheaders/Bitmap::Bitmap
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
 - Bitmap.Bitmap
---

# Bitmap::Bitmap(IN const BITMAPINFO,IN VOID)


## -description

Creates a <b>Bitmap::Bitmap</b> object based on a 
			<b>BITMAPINFO</b> structure and an array of pixel data.

## -parameters

### -param gdiBitmapInfo [in]

Type: <b>const <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>*</b>

Pointer to a GDI <b>BITMAPINFO</b> structure. This structure defines several bitmap attributes, such as size and pixel format. The 
					<b>BITMAPINFO</b> structure is defined in Wingdi.h.

### -param gdiBitmapData [in]

Type: <b>VOID*</b>

Pointer to an array of bytes that contains the pixel data.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-frombitmapinfo">Bitmap::FromBITMAPINFO</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>