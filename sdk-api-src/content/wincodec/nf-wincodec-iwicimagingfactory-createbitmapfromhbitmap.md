---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWICImagingFactory::CreateBitmapFromHBITMAP


## -description


Creates an <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> from a bitmap handle.


## -parameters




### -param hBitmap [in]

Type: <b>HBITMAP</b>

A bitmap handle to create the bitmap from.


### -param hPalette [in]

Type: <b>HPALETTE</b>

A palette handle used to create the bitmap.


### -param options [in]

Type: <b><a href="https://msdn.microsoft.com/caa10c35-9af4-4310-b031-3347cf795087">WICBitmapAlphaChannelOption</a></b>

The alpha channel options to create the bitmap.


### -param ppIBitmap [out]

Type: <b><a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>**</b>

A pointer that receives a pointer to the new bitmap.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For a non-palletized bitmap, set NULL for the <i>hPalette</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">GDI+ Bitmap class</a>



<a href="https://msdn.microsoft.com/9728a458-fd25-4edf-bf9e-c38766934dd4">GDI+ Bitmap.GetHBITMAP method</a>



<a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>



<a href="https://msdn.microsoft.com/caa10c35-9af4-4310-b031-3347cf795087">WICBitmapAlphaChannelOption</a>
 

 

