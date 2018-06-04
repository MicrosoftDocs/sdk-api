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

# IWICBitmapSourceTransform::GetClosestPixelFormat


## -description


Retrieves the closest pixel format to which the implementation of <a href="https://msdn.microsoft.com/f9cc348f-d4f0-4e77-90d6-9ff563a1799c">IWICBitmapSourceTransform</a> can natively copy pixels, given a desired format.


## -parameters




### -param pguidDstFormat [in, out]

Type: <b>WICPixelFormatGUID*</b>

A pointer that receives the GUID of the pixel format that is the closest supported pixel format of the desired format.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Windows provided codecs provide the following support:

<ul>
<li>BMP, ICO, GIF, TIFF: No implementation of <a href="https://msdn.microsoft.com/f9cc348f-d4f0-4e77-90d6-9ff563a1799c">IWICBitmapSourceTransform</a>.</li>
<li>JPEG, PNG, JPEG-XR: Trivial support (always returns the same value as <a href="https://msdn.microsoft.com/6fd30a38-a447-4e4e-93ea-e31c5ba1271e">IWICBitmapFrameDecode::GetPixelFormat</a>).</li>
</ul>


