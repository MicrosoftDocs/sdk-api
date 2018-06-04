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

# IWMPlayerTimestampHook::MapTimestamp


## -description



The <b>MapTimestamp</b> method is called by the WMV Decoder DMO to enable the source filter to provide the decoder with a time stamp. The decoder applies the time stamp to the sample before delivering the sample to the video renderer.




## -parameters




### -param rtIn [in]

Time stamp previously applied by the DMO.


### -param prtOut [out]

Time stamp to be applied to the sample.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code .




## -see-also




<a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>



<a href="https://msdn.microsoft.com/8a1b3b1f-1c9c-429f-958e-757b383c7e2a">IWMPlayerTimestampHook Interface</a>
 

 

