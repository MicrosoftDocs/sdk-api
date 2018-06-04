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

# IWICPixelFormatInfo::GetChannelMask


## -description


Gets the pixel format's channel mask.


## -parameters




### -param uiChannelIndex [in]

Type: <b>UINT</b>

The index to the channel mask to retrieve.


### -param cbMaskBuffer [in]

Type: <b>UINT</b>

The size of the <i>pbMaskBuffer</i> buffer.


### -param pbMaskBuffer [in, out]

Type: <b>BYTE*</b>

Pointer to the mask buffer.


### -param pcbActual [out]

Type: <b>UINT*</b>

The actual buffer size needed to obtain the channel mask.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If 0 and NULL are passed in for <i>cbMaskBuffer</i> and <i>pbMaskBuffer</i>, respectively, the required buffer size will be returned through <i>pcbActual</i>.




