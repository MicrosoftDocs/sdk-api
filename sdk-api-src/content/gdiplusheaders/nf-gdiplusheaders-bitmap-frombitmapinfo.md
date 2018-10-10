---
UID: NF:gdiplusheaders.Bitmap.FromBITMAPINFO
title: Bitmap::FromBITMAPINFO
author: windows-sdk-content
description: The Bitmap::FromBITMAPINFO method creates a Bitmap object based on a BITMAPINFO structure and an array of pixel data.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_FromBITMAPINFO_gdiBitmapInfo_gdiBitmapData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\frombitmapinfo.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Bitmap class [GDI+],FromBITMAPINFO method, Bitmap.FromBITMAPINFO, Bitmap::FromBITMAPINFO, FromBITMAPINFO, FromBITMAPINFO method [GDI+], FromBITMAPINFO method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_FromBITMAPINFO_gdiBitmapInfo_gdiBitmapData_, gdiplus._gdiplus_CLASS_Bitmap_FromBITMAPINFO_gdiBitmapInfo_gdiBitmapData_
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
 - Bitmap.FromBITMAPINFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Bitmap::FromBITMAPINFO


## -description


The <b>Bitmap::FromBITMAPINFO</b> method creates a 
			<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object based on a 
			<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure and an array of pixel data.


## -parameters




### -param gdiBitmapInfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>*</b>

Pointer to a GDI 
					<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure. This structure defines several bitmap attributes, such as size and pixel format. The 
					BITMAPINFO structure is defined in Wingdi.h. 


### -param gdiBitmapData [in]

Type: <b>VOID*</b>

Pointer to an array of bytes that contains the pixel data. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a> object.




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

