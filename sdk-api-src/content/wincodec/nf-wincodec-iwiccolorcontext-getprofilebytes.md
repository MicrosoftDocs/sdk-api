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

# IWICColorContext::GetProfileBytes


## -description


Retrieves the color context profile.


## -parameters




### -param cbBuffer [in]

Type: <b>UINT</b>

The size of the <i>pbBuffer</i> buffer.


### -param pbBuffer [in, out]

Type: <b>BYTE*</b>

A pointer that receives the color context profile.


### -param pcbActual [out]

Type: <b>UINT*</b>

A pointer that receives the actual buffer size needed to retrieve the entire color context profile.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Only use this method if the context type is <a href="_wic_codec_wiccolorcontexttype.htm">WICColorContextProfile</a>.


Calling this method with <i>pbBuffer</i> set to <b>NULL</b> will cause it to return the required buffer size in <i>pcbActual</i>.




