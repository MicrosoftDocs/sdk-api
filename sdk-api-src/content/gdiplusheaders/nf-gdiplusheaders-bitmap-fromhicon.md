---
UID: NF:gdiplusheaders.Bitmap.FromHICON
title: Bitmap::FromHICON (gdiplusheaders.h)
description: The Bitmap::FromHICON method creates a Bitmap object based on a handle to an icon.
helpviewer_keywords: ["Bitmap class [GDI+]","FromHICON method","Bitmap.FromHICON","Bitmap::FromHICON","FromHICON","FromHICON method [GDI+]","FromHICON method [GDI+]","Bitmap class","_gdiplus_CLASS_Bitmap_FromHICON_hicon_","gdiplus._gdiplus_CLASS_Bitmap_FromHICON_hicon_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_FromHICON_hicon_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\fromhicon.htm
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],FromHICON method, Bitmap.FromHICON, Bitmap::FromHICON, FromHICON, FromHICON method [GDI+], FromHICON method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_FromHICON_hicon_, gdiplus._gdiplus_CLASS_Bitmap_FromHICON_hicon_
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
 - Bitmap::FromHICON
 - gdiplusheaders/Bitmap::FromHICON
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
 - Bitmap.FromHICON
---

# Bitmap::FromHICON


## -description

The <b>Bitmap::FromHICON</b> method creates a 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object based on a handle to an icon.

## -parameters

### -param hicon [in]

Type: <b>HICON</b>

Handle to a GDI icon.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>*</b>

This method returns a pointer to the new 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>