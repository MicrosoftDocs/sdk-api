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

# IWICBitmapSourceTransform::DoesSupportTransform


## -description


Determines whether a specific transform option is supported natively by the implementation of the <a href="https://msdn.microsoft.com/f9cc348f-d4f0-4e77-90d6-9ff563a1799c">IWICBitmapSourceTransform</a> interface.


## -parameters




### -param dstTransform [in]

Type: <b><a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a></b>

The <a href="https://msdn.microsoft.com/e123bb4d-bc75-4f3f-98f1-bea9b008498b">WICBitmapTransformOptions</a> to check if they are supported.


### -param pfIsSupported [out]

Type: <b>BOOL*</b>

A pointer that receives a value specifying whether the transform option is supported.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Windows provided codecs provide the following level of support:

<ul>
<li>BMP, ICO, GIF, TIFF: No implementation of <a href="https://msdn.microsoft.com/6a3e682c-55c6-4728-9d14-5eb0290f3dcc">IWICBitmapSourceTransform</a>.</li>
<li>JPEG, PNG: Trivial support (WICBitmapTransformRotate0 only).</li>
<li>JPEG-XR: Support for all transformation/rotations.
</li>
</ul>


