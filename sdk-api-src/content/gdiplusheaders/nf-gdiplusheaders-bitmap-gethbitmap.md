---
UID: NF:gdiplusheaders.Bitmap.GetHBITMAP
title: Bitmap::GetHBITMAP (gdiplusheaders.h)
author: windows-sdk-content
description: The Bitmap::GetHBITMAP method creates a Windows Graphics Device Interface (GDI) bitmap from this Bitmap object.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_GetHBITMAP_colorBackground_hbmReturn_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\gethbitmap.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],GetHBITMAP method, Bitmap.GetHBITMAP, Bitmap::GetHBITMAP, GetHBITMAP, GetHBITMAP method [GDI+], GetHBITMAP method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_GetHBITMAP_colorBackground_hbmReturn_, gdiplus._gdiplus_CLASS_Bitmap_GetHBITMAP_colorBackground_hbmReturn_
ms.topic: method
f1_keywords: 
 - "gdiplusheaders/Bitmap.GetHBITMAP"
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
 - Bitmap.GetHBITMAP
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Bitmap::GetHBITMAP


## -description


The <b>Bitmap::GetHBITMAP</b> method creates a Windows Graphics Device Interface (GDI) bitmap from this 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object.


## -parameters




### -param colorBackground [in, ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a 
					<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the background color. This parameter is ignored if the bitmap is totally opaque. 


### -param hbmReturn [out]

Type: <b>HBITMAP*</b>

Pointer to an 
					<b>HBITMAP</b> that receives a handle to the GDI bitmap. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>
 

 

