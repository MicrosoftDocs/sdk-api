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

# IMILBitmapEffectPrimitive::TransformPoint


## -description


Transforms the given point.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating the output pin through which to transform the point.


### -param p [in, out]

Type: <b><a href="https://msdn.microsoft.com/5898a130-c7d2-4880-9a2a-2dcd2d984605">MIL_2DPOINTD</a>*</b>

A pointer to the point to transform.


### -param fForwardTransform [in]

Type: <b>VARIANT_BOOL</b>

A value indicating whether the point is being transformed from front to back in the effects graph.


### -param pContext [in]

Type: <b><a href="https://msdn.microsoft.com/0c8fbbba-32e6-459c-90ab-2453b57c27ee">IMILBitmapEffectRenderContext</a>*</b>

The render context to use for the transformation.


### -param pfPointTransformed [out]

Type: <b>VARIANT_BOOL*</b>

When this method returns, contains a value indicating whether the point transformed to a known location.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



