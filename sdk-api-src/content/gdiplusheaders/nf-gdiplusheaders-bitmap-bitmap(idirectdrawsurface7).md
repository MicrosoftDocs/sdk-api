---
UID: NF:gdiplusheaders.Bitmap.Bitmap(IDirectDrawSurface7)
title: Bitmap::Bitmap(IN IDirectDrawSurface7) (gdiplusheaders.h)
description: Creates a Bitmap::Bitmap object based on a DirectDraw surface. The Bitmap::Bitmap object maintains a reference to the DirectDraw surface until the Bitmap::Bitmap object is deleted or goes out of scope.
helpviewer_keywords: ["Bitmap","Bitmap class [GDI+]","Bitmap constructor","Bitmap constructor [GDI+]","Bitmap constructor [GDI+]","Bitmap class","Bitmap.Bitmap","Bitmap.Bitmap(IDirectDrawSurface7*)","Bitmap.Bitmap(IN IDirectDrawSurface7)","Bitmap::Bitmap","Bitmap::Bitmap(IN IDirectDrawSurface7)","_gdiplus_CLASS_Bitmap_Bitmap_surface_","gdiplus._gdiplus_CLASS_Bitmap_Bitmap_surface_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Bitmap_surface_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapconstructors\bitmap_15surface.htm
ms.date: 12/05/2018
ms.keywords: Bitmap, Bitmap class [GDI+],Bitmap constructor, Bitmap constructor [GDI+], Bitmap constructor [GDI+],Bitmap class, Bitmap.Bitmap, Bitmap.Bitmap(IDirectDrawSurface7*), Bitmap.Bitmap(IN IDirectDrawSurface7), Bitmap::Bitmap, Bitmap::Bitmap(IN IDirectDrawSurface7), _gdiplus_CLASS_Bitmap_Bitmap_surface_, gdiplus._gdiplus_CLASS_Bitmap_Bitmap_surface_
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

# Bitmap::Bitmap(IN IDirectDrawSurface7)


## -description

Creates a <b>Bitmap::Bitmap</b> object based on a DirectDraw surface. The <b>Bitmap::Bitmap</b> object maintains a reference to the DirectDraw surface until the <b>Bitmap::Bitmap</b> object is deleted or goes out of scope.

## -parameters

### -param surface [in]

Type: <b>IDirectDrawSurface7*</b>

Pointer to an 
					<b>IDrectDrawSurface7</b> COM interface.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-fromdirectdrawsurface7">Bitmap::FromDirectDrawSurface7</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>