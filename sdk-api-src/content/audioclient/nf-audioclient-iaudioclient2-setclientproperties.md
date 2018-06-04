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

# IAudioClient2::SetClientProperties


## -description


Sets the properties of the audio stream by populating an <a href="https://msdn.microsoft.com/5BCCD581-DB66-4939-A62A-2236B9E49AA7">AudioClientProperties</a> structure.


## -parameters




### -param pProperties [in]

Pointer to an <a href="https://msdn.microsoft.com/5BCCD581-DB66-4939-A62A-2236B9E49AA7">AudioClientProperties</a> structure.


## -returns



The <b>SetClientProperties</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -remarks



Starting with Windows 10, hardware-offloaded audio streams must be event driven. This means that if you call <b>IAudioClient2::SetClientProperties</b> and set the <i>bIsOffload</i> parameter of the <a href="https://msdn.microsoft.com/5BCCD581-DB66-4939-A62A-2236B9E49AA7">AudioClientProperties</a> to TRUE, you must specify the <b>AUDCLNT_STREAMFLAGS_EVENTCALLBACK</b> flag in the <i>StreamFlags</i> parameter to <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>.




## -see-also




<a href="https://msdn.microsoft.com/5BCCD581-DB66-4939-A62A-2236B9E49AA7">AudioClientProperties</a>



<a href="https://msdn.microsoft.com/9CE79CEB-115E-4802-A687-B2CB23E6A0E0">IAudioClient2</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>
 

 

