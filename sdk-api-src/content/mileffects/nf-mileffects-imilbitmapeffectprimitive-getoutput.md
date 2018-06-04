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

# IMILBitmapEffectPrimitive::GetOutput


## -description


Performs pixel processing for the bitmap effect.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating which output pin to use for output.


### -param pContext [in]

Type: <b><a href="https://msdn.microsoft.com/0c8fbbba-32e6-459c-90ab-2453b57c27ee">IMILBitmapEffectRenderContext</a>*</b>

The render context to use to determine how the effect should be rendered.


### -param pfModifyInPlace [in, out]

Type: <b>VARIANT_BOOL*</b>

A value that indicates whether the effect should attempt to modify the input image in place.


### -param ppBitmapSource [out, retval]

Type: <b>IWICBitmapSource**</b>

When this method returns, contains a pointer to the effect output.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            If <i>pfModifyInPlace</i> is VARIANT_TRUE, the input image may be modified and returned.
            If the custom effect does not support in place modifications, set <i>pfModifyInPlace</i> to VARIANT_FALSE to indicate a new image was created.
         



