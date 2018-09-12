---
UID: NF:gdiplusheaders.Bitmap.GetHBITMAP
title: Bitmap::GetHBITMAP
author: windows-sdk-content
description: The Bitmap::GetHBITMAP method creates a Windows Graphics Device Interface (GDI) bitmap from this Bitmap object.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_GetHBITMAP_colorBackground_hbmReturn_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\gethbitmap.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Bitmap class [GDI+],GetHBITMAP method, Bitmap.GetHBITMAP, Bitmap::GetHBITMAP, GetHBITMAP, GetHBITMAP method [GDI+], GetHBITMAP method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_GetHBITMAP_colorBackground_hbmReturn_, gdiplus._gdiplus_CLASS_Bitmap_GetHBITMAP_colorBackground_hbmReturn_
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
 - Bitmap.GetHBITMAP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Bitmap::GetHBITMAP


## -description


The <b>Bitmap::GetHBITMAP</b> method creates a Windows Graphics Device Interface (GDI) bitmap from this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> object.


## -parameters




### -param colorBackground [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a></b>

Reference to a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a> object that specifies the background color. This parameter is ignored if the bitmap is totally opaque. 


### -param hbmReturn [out]

Type: <b>HBITMAP*</b>

Pointer to an 
					<b>HBITMAP</b> that receives a handle to the GDI bitmap. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536335(v=VS.85).aspx">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533815(v=VS.85).aspx">Using Images, Bitmaps, and Metafiles</a>
 

 

