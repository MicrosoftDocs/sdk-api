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

# IWICDevelopRaw::GetToneCurve


## -description


Gets the tone curve of the raw image.


## -parameters




### -param cbToneCurveBufferSize [in]

Type: <b>UINT</b>

The size of the <i>pToneCurve</i> buffer.


### -param pToneCurve [out]

Type: <b><a href="https://msdn.microsoft.com/45eedc32-a642-4ef6-a02a-63eaeacf0012">WICRawToneCurve</a>*</b>

A pointer that receives the <a href="https://msdn.microsoft.com/45eedc32-a642-4ef6-a02a-63eaeacf0012">WICRawToneCurve</a> of the raw image.


### -param pcbActualToneCurveBufferSize [out]

Type: <b>UINT*</b>

A pointer that receives the size needed to obtain the tone curve structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



