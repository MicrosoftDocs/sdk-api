---
UID: NF:gdiplusheaders.Bitmap.Bitmap(IN HINSTANCE,IN const WCHAR)
title: Bitmap::Bitmap(IN HINSTANCE,IN const WCHAR) (gdiplusheaders.h)
author: windows-sdk-content
description: Creates a Bitmap::Bitmap object based on an application or DLL instance handle and the name of a bitmap resource.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Bitmap_hInstance_bitmapName_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapconstructors\bitmap_56hinstance_bitmapname.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Bitmap, Bitmap class [GDI+],Bitmap constructor, Bitmap constructor [GDI+], Bitmap constructor [GDI+],Bitmap class, Bitmap.Bitmap, Bitmap.Bitmap(HINSTANCE,const WCHAR*), Bitmap.Bitmap(IN HINSTANCE,IN const WCHAR), Bitmap::Bitmap, Bitmap::Bitmap(IN HINSTANCE,IN const WCHAR), _gdiplus_CLASS_Bitmap_Bitmap_hInstance_bitmapName_, gdiplus._gdiplus_CLASS_Bitmap_Bitmap_hInstance_bitmapName_
ms.topic: method
f1_keywords: 
 - "gdiplusheaders/Bitmap.Bitmap"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Bitmap.Bitmap
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Bitmap::Bitmap(IN HINSTANCE,IN const WCHAR)


## -description


Creates a <b>Bitmap::Bitmap</b> object based on an application or DLL instance handle and the name of a bitmap resource.


## -parameters




### -param hInstance [in]

Type: <b>HINSTANCE</b>

Handle to an instance of a module whose executable file contains a bitmap resource. 


### -param bitmapName [in]

Type: <b>const WCHAR*</b>

Pointer to a null-terminated string that specifies the path name of the bitmap resource to be loaded. Alternatively, this parameter can consist of the resource identifier in the low-order word and zero in the high-order word. You can use the 
					<b>MAKEINTRESOURCE</b> macro to create this value. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-fromresource">Bitmap::FromResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>
 

 

