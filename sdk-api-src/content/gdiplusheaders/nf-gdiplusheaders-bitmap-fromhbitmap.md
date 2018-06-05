---
UID: NF:gdiplusheaders.Bitmap.FromHBITMAP
title: Bitmap::FromHBITMAP
author: windows-sdk-content
description: The Bitmap::FromHBITMAP method creates a Bitmap object based on a handle to a Windows Graphics Device Interface (GDI) bitmap and a handle to a GDI palette.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_FromHBITMAP_hbm_hpal_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\fromhbitmap.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Bitmap class [GDI+],FromHBITMAP method, Bitmap.FromHBITMAP, Bitmap::FromHBITMAP, FromHBITMAP, FromHBITMAP method [GDI+], FromHBITMAP method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_FromHBITMAP_hbm_hpal_, gdiplus._gdiplus_CLASS_Bitmap_FromHBITMAP_hbm_hpal_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Bitmap.FromHBITMAP
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Bitmap::FromHBITMAP


## -description


The <b>Bitmap::FromHBITMAP</b> method creates a 
			<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object based on a handle to a Windows Graphics Device Interface (GDI) bitmap and a handle to a GDI palette.


## -parameters




### -param hbm [in]

Type: <b>HBITMAP</b>

Handle to GDI bitmap. 


### -param hpal [in]

Type: <b>HPALETTE</b>

Handle to a GDI palette used to define the bitmap colors if 
					<i>hbm</i> is not a device-independent bitmap (DIB). 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object.




## -remarks



You are responsible for deleting the GDI bitmap and the GDI palette. However, you should not delete the GDI bitmap or the GDI palette until after the GDI+ 
				<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object is deleted or goes out of scope.

Do not pass to the <b>Bitmap::FromHBITMAP</b> method a GDI bitmap or a GDI palette that is currently (or was previously) selected into a device context.

This method does not preserve the alpha channel of the source GDI bitmap.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

