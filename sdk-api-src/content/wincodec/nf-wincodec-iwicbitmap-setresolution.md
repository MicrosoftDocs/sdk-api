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

# IWICBitmap::SetResolution


## -description


Changes the physical resolution of the image.


## -parameters




### -param dpiX [in]

Type: <b>double</b>

The horizontal resolution.


### -param dpiY [in]

Type: <b>double</b>

The vertical resolution.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            This method has no effect on the actual pixels or samples stored in the bitmap. 
            Instead the interpretation of the sampling rate is modified. 
            This means that a 96 DPI image which is 96 pixels wide is one inch. 
            If the physical resolution is modified to 48 DPI, then the bitmap is considered to be 2 inches wide but has the same number of pixels.  
            If the resolution is less than <b>REAL_EPSILON</b> (1.192092896e-07F) the error code <b>WINCODEC_ERR_INVALIDPARAMETER</b> is returned.



