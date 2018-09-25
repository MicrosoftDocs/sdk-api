---
UID: NF:gdiplusheaders.Bitmap.FromStream
title: Bitmap::FromStream
author: windows-sdk-content
description: The Bitmap::FromStream method creates a Bitmap object based on a stream.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_FromStream_stream_useEmbeddedColorManagement_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\fromstream.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: Bitmap class [GDI+],FromStream method, Bitmap.FromStream, Bitmap::FromStream, FromStream, FromStream method [GDI+], FromStream method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_FromStream_stream_useEmbeddedColorManagement_, gdiplus._gdiplus_CLASS_Bitmap_FromStream_stream_useEmbeddedColorManagement_
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
 - Bitmap.FromStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Bitmap::FromStream


## -description


The <b>Bitmap::FromStream</b> method creates a 
			<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object based on a stream.


## -parameters




### -param stream [in]

Type: <b><a href="_stg_istream">IStream</a>*</b>

Pointer to an 
					<a href="_stg_istream">IStream</a>COMCOM interface. The implementation of 
					IStream must include the 
					<a href="_stg_istream_seek">IStream::Seek</a>, 
					<b>Read</b>, and 
					<a href="_stg_istream_stat">IStream::Stat</a> methods. 


### -param useEmbeddedColorManagement [in]

Type: <b>BOOL</b>

Optional. <b>BOOL</b> value that specifies whether the new 
					<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object applies color correction according to color management information that is embedded in the stream. Embedded information can include International Color Consortium (ICC) profiles, gamma values, and chromaticity information. <b>TRUE</b> specifies that color correction is enabled, and <b>FALSE</b> specifies that color correction is not enabled. The default value is <b>FALSE</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object.




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

