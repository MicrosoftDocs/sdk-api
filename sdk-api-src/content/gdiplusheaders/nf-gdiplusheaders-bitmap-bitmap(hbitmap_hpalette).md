---
UID: NF:gdiplusheaders.Bitmap.Bitmap(HBITMAP,HPALETTE)
title: Bitmap::Bitmap(IN HBITMAP,IN HPALETTE) (gdiplusheaders.h)
description: Creates a Bitmap::Bitmap object based on a handle to a Windows Windows Graphics Device Interface (GDI) bitmap and a handle to a GDI palette.
helpviewer_keywords: ["Bitmap","Bitmap class [GDI+]","Bitmap constructor","Bitmap constructor [GDI+]","Bitmap constructor [GDI+]","Bitmap class","Bitmap.Bitmap","Bitmap.Bitmap(HBITMAP","HPALETTE)","Bitmap.Bitmap(IN HBITMAP","IN HPALETTE)","Bitmap::Bitmap","Bitmap::Bitmap(IN HBITMAP","IN HPALETTE)","_gdiplus_CLASS_Bitmap_Bitmap_hbm_hpal_","gdiplus._gdiplus_CLASS_Bitmap_Bitmap_hbm_hpal_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Bitmap_hbm_hpal_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapconstructors\bitmap_52hbm_hpal.htm
ms.date: 12/05/2018
ms.keywords: Bitmap, Bitmap class [GDI+],Bitmap constructor, Bitmap constructor [GDI+], Bitmap constructor [GDI+],Bitmap class, Bitmap.Bitmap, Bitmap.Bitmap(HBITMAP,HPALETTE), Bitmap.Bitmap(IN HBITMAP,IN HPALETTE), Bitmap::Bitmap, Bitmap::Bitmap(IN HBITMAP,IN HPALETTE), _gdiplus_CLASS_Bitmap_Bitmap_hbm_hpal_, gdiplus._gdiplus_CLASS_Bitmap_Bitmap_hbm_hpal_
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

# Bitmap::Bitmap(IN HBITMAP,IN HPALETTE)


## -description

Creates a <b>Bitmap::Bitmap</b> object based on a handle to a Windows Windows Graphics Device Interface (GDI) bitmap and a handle to a GDI palette.

## -parameters

### -param hbm [in]

Type: <b>HBITMAP</b>

Handle to a GDI bitmap.

### -param hpal [in]

Type: <b>HPALETTE</b>

Handle to a GDI palette used to define the bitmap colors if 
					<i>hbm</i> is not a device-independent bitmap (DIB).

## -remarks

You are responsible for deleting the GDI bitmap and the GDI palette. However, you should not delete the GDI bitmap or the GDI palette until after the GDI+ <b>Bitmap::Bitmap</b> object is deleted or goes out of scope.

Do not pass to the GDI+ <b>Bitmap::Bitmap</b> constructor a GDI bitmap or a GDI palette that is currently (or was previously) selected into a device context.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-fromhbitmap">Bitmap::FromHBITMAP</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>