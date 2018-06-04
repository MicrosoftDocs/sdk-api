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

# IWTSBitmapRendererCallback::OnTargetSizeChanged


## -description


Called when the size of the render target has changed. The image passed to <a href="https://msdn.microsoft.com/536c6954-0cde-48d1-ba5b-a97c9942f0f6">IWTSBitmapRenderer::Render</a> must conform to this size.


## -parameters




### -param rcNewSize [in]

A <b>RECT</b> structure that contains the new size of the render target.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bdb8280b-6ebc-47e4-9789-47e3bda96efc">IWTSBitmapRendererCallback</a>
 

 

