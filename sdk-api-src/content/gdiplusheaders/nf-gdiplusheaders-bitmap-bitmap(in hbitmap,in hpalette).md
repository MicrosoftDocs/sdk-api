---
UID: NF:gdiplusheaders.Bitmap.Bitmap(IN HBITMAP,IN HPALETTE)
title: Bitmap::Bitmap(IN HBITMAP,IN HPALETTE)
author: windows-sdk-content
description: Creates a Bitmap::Bitmap object based on a handle to a Windows Windows Graphics Device Interface (GDI) bitmap and a handle to a GDI palette.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Bitmap_hbm_hpal_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapconstructors\bitmap_52hbm_hpal.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Bitmap, Bitmap class [GDI+],Bitmap constructor, Bitmap constructor [GDI+], Bitmap constructor [GDI+],Bitmap class, Bitmap.Bitmap, Bitmap.Bitmap(HBITMAP,HPALETTE), Bitmap.Bitmap(IN HBITMAP,IN HPALETTE), Bitmap::Bitmap, Bitmap::Bitmap(IN HBITMAP,IN HPALETTE), _gdiplus_CLASS_Bitmap_Bitmap_hbm_hpal_, gdiplus._gdiplus_CLASS_Bitmap_Bitmap_hbm_hpal_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
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




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="https://msdn.microsoft.com/08b970fe-b548-4fb7-8dea-63eef8a36510">Bitmap::FromHBITMAP</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

