---
UID: NF:gdiplusheaders.Bitmap.FromResource
title: Bitmap::FromResource
author: windows-sdk-content
description: The Bitmap::FromResource method creates a Bitmap object based on an application or DLL instance handle and the name of a bitmap resource.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_FromResource_hInstance_bitmapName_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\fromresource.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Bitmap class [GDI+],FromResource method, Bitmap.FromResource, Bitmap::FromResource, FromResource, FromResource method [GDI+], FromResource method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_FromResource_hInstance_bitmapName_, gdiplus._gdiplus_CLASS_Bitmap_FromResource_hInstance_bitmapName_
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Bitmap.FromResource
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Bitmap::FromResource


## -description


The <b>Bitmap::FromResource</b> method creates a 
			<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object based on an application or DLL instance handle and the name of a bitmap resource.


## -parameters




### -param hInstance [in]

Type: <b>HINSTANCE</b>

Handle to an instance of a module whose executable file contains a bitmap resource. 


### -param bitmapName [in]

Type: <b>const WCHAR*</b>

Pointer to a null-terminated string that specifies the path name of the bitmap resource to be loaded. Alternatively, this parameter can consist of the resource identifier in the low-order word and zero in the high-order word. You can use the 
					<a href="_win32_makeintresource">MAKEINTRESOURCE</a> macro to create this value. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

