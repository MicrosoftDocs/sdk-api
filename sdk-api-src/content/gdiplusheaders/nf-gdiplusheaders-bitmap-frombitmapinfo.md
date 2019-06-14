---
UID: NF:gdiplusheaders.Bitmap.FromBITMAPINFO
title: Bitmap::FromBITMAPINFO (gdiplusheaders.h)
author: windows-sdk-content
description: The Bitmap::FromBITMAPINFO method creates a Bitmap object based on a BITMAPINFO structure and an array of pixel data.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_FromBITMAPINFO_gdiBitmapInfo_gdiBitmapData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\frombitmapinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],FromBITMAPINFO method, Bitmap.FromBITMAPINFO, Bitmap::FromBITMAPINFO, FromBITMAPINFO, FromBITMAPINFO method [GDI+], FromBITMAPINFO method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_FromBITMAPINFO_gdiBitmapInfo_gdiBitmapData_, gdiplus._gdiplus_CLASS_Bitmap_FromBITMAPINFO_gdiBitmapInfo_gdiBitmapData_
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
 - Bitmap.FromBITMAPINFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Bitmap::FromBITMAPINFO


## -description


The <b>Bitmap::FromBITMAPINFO</b> method creates a 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object based on a 
			<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a> structure and an array of pixel data.


## -parameters




### -param gdiBitmapInfo [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a>*</b>

Pointer to a GDI 
					<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagbitmapinfo">BITMAPINFO</a> structure. This structure defines several bitmap attributes, such as size and pixel format. The 
					BITMAPINFO structure is defined in Wingdi.h. 


### -param gdiBitmapData [in]

Type: <b>VOID*</b>

Pointer to an array of bytes that contains the pixel data. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>
 

 

