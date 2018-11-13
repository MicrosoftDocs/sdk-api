---
UID: NF:gdiplusheaders.Bitmap.Bitmap(IN IStream,IN BOOL)
title: Bitmap::Bitmap(IN IStream,IN BOOL)
author: windows-sdk-content
description: Creates a Bitmap::Bitmap object based on an IStream COM interface.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Bitmap_stream_useIcm_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapconstructors\bitmap_90stream_useicm.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Bitmap, Bitmap class [GDI+],Bitmap constructor, Bitmap constructor [GDI+], Bitmap constructor [GDI+],Bitmap class, Bitmap.Bitmap, Bitmap.Bitmap(IN IStream,IN BOOL), Bitmap.Bitmap(IStream*,BOOL), Bitmap::Bitmap, Bitmap::Bitmap(IN IStream,IN BOOL), _gdiplus_CLASS_Bitmap_Bitmap_stream_useIcm_, gdiplus._gdiplus_CLASS_Bitmap_Bitmap_stream_useIcm_
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

# Bitmap::Bitmap(IN IStream,IN BOOL)


## -description


Creates a <b>Bitmap::Bitmap</b> object based on an <b>IStream</b> COM interface.


## -parameters




### -param stream [in]

Type: <b><a href="_stg_istream">IStream</a>*</b>

Pointer to an 
					<b>IStream</b> COM interface.


### -param useEmbeddedColorManagement

TBD




#### - useIcm [in]

Type: <b>BOOL</b>

Boolean value that specifies whether the new <b>Bitmap::Bitmap</b> object applies color correction according to color management information that is embedded in the stream (represented by the <b>stream</b> parameter). Embedded information can include International Color Consortium (ICC) profiles, gamma values, and chromaticity information. <b>TRUE</b> specifies that color correction is enabled, and <b>FALSE</b> specifies that color correction is not enabled. The default value is <b>FALSE</b>. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="https://msdn.microsoft.com/9ba75f67-b06e-4115-b2af-2fff95715d94">Bitmap::FromStream</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

