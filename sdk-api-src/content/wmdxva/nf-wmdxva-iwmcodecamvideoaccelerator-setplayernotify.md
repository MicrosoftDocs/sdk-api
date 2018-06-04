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

# IWMCodecAMVideoAccelerator::SetPlayerNotify


## -description



The <b>SetPlayerNotify</b> method is called by the output pin on the source filter to provide the decoder <a href="wmformat_glossary.htm">DMO</a> with the source filter's <b>IWMPlayerTimestampHook</b> interface to enable the source filter to update the time stamps on the samples before they are delivered to the renderer.




## -parameters




### -param pHook [in]

Pointer to the <b>IWMPlayerTimestampHook</b> interface exposed on the player.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code




## -see-also




<a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>



<a href="https://msdn.microsoft.com/48cfc4d1-4b79-47a5-9cc9-a1f19d2c0123">IWMCodecAMVideoAccelerator Interface</a>
 

 

