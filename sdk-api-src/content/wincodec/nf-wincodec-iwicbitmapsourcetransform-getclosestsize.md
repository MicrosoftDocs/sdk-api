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

# IWICBitmapSourceTransform::GetClosestSize


## -description


Returns the closest dimensions the implementation can natively scale to given the desired dimensions.


## -parameters




### -param puiWidth [in, out]

Type: <b>UINT*</b>

The desired width. A pointer that receives the closest supported width.


### -param puiHeight [in, out]

Type: <b>UINT*</b>

The desired height. A pointer that receives the closest supported height.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Windows provided codecs provide the following support for native scaling:


<ul>
<li>BMP, ICO, GIF, TIFF: No implementation of <a href="https://msdn.microsoft.com/6a3e682c-55c6-4728-9d14-5eb0290f3dcc">IWICBitmapSourceTransform</a>.</li>
<li>PNG: No scaling support.</li>
<li>JPEG: Native down-scaling by a factor of 8, 4, or 2.</li>
<li>JPEG-XR:  Native scaling of the original image by powers of 2.
</li>
</ul>


