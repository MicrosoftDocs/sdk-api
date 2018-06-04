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

# IWICBitmapSource::GetResolution


## -description


Retrieves the sampling rate between pixels and physical world measurements.


## -parameters




### -param pDpiX [out]

Type: <b>double*</b>

A pointer that receives the x-axis dpi resolution.


### -param pDpiY [out]

Type: <b>double*</b>

A pointer that receives the y-axis dpi resolution.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            Some formats, such as GIF and ICO, do not have full DPI support.
             For GIF, this method calculates the DPI values from the aspect ratio, using a base DPI of (96.0, 96.0).
            The ICO format does not support DPI at all, and the method always returns (96.0,96.0) for ICO images.
         


            Additionally, WIC itself does not transform images based on the DPI values in an image.
            It is up to the caller to transform an image based on the resolution returned.
         



