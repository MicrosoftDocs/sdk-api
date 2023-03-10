---
UID: NF:gdiplusheaders.Bitmap.FromResource
title: Bitmap::FromResource (gdiplusheaders.h)
description: The Bitmap::FromResource method creates a Bitmap object based on an application or DLL instance handle and the name of a bitmap resource.
helpviewer_keywords: ["Bitmap class [GDI+]","FromResource method","Bitmap.FromResource","Bitmap::FromResource","FromResource","FromResource method [GDI+]","FromResource method [GDI+]","Bitmap class","_gdiplus_CLASS_Bitmap_FromResource_hInstance_bitmapName_","gdiplus._gdiplus_CLASS_Bitmap_FromResource_hInstance_bitmapName_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_FromResource_hInstance_bitmapName_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\fromresource.htm
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],FromResource method, Bitmap.FromResource, Bitmap::FromResource, FromResource, FromResource method [GDI+], FromResource method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_FromResource_hInstance_bitmapName_, gdiplus._gdiplus_CLASS_Bitmap_FromResource_hInstance_bitmapName_
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
 - Bitmap::FromResource
 - gdiplusheaders/Bitmap::FromResource
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
 - Bitmap.FromResource
---

# Bitmap::FromResource


## -description

The <b>Bitmap::FromResource</b> method creates a 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object based on an application or DLL instance handle and the name of a bitmap resource.

## -parameters

### -param hInstance [in]

Type: <b>HINSTANCE</b>

Handle to an instance of a module whose executable file contains a bitmap resource.

### -param bitmapName [in]

Type: <b>const WCHAR*</b>

Pointer to a null-terminated string that specifies the path name of the bitmap resource to be loaded. Alternatively, this parameter can consist of the resource identifier in the low-order word and zero in the high-order word. You can use the 
					<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro to create this value.

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