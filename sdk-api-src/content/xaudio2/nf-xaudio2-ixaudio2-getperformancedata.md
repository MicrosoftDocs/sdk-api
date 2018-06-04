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

# IXAudio2::GetPerformanceData


## -description


Returns current resource usage details, such as available memory or CPU usage.


## -parameters




### -param pPerfData [out]

On success, pointer to an <a href="https://msdn.microsoft.com/10808e6b-50e8-4254-9e0c-b8047a15fda5">XAUDIO2_PERFORMANCE_DATA</a> structure that is returned. 



## -returns



This method does not return a value.




## -remarks



For specific information on the statistics returned by <b>GetPerformanceData</b>, see the <a href="https://msdn.microsoft.com/10808e6b-50e8-4254-9e0c-b8047a15fda5">XAUDIO2_PERFORMANCE_DATA</a> structure reference.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/A49469C6-2C29-407C-8C57-65E3FC9463F1">IXAudio2</a>
 

 

