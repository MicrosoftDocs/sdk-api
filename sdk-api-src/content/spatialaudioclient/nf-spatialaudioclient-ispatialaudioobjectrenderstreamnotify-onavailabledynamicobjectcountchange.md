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

# ISpatialAudioObjectRenderStreamNotify::OnAvailableDynamicObjectCountChange


## -description


Notifies the spatial audio client when the rendering capacity for an <a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a> is about to change, specifies the time after which the change will occur, and specifies the number of dynamic audio objects that will be available after the change.


## -parameters




### -param sender [in]

The spatial audio render stream for which the available dynamic object count is changing.


### -param hnsComplianceDeadlineTime [in]

The time after which the spatial resource limit will change, in 100-nanosecond units. A value of  0 means that the change will occur immediately.


### -param availableDynamicObjectCountChange [in]

The number of dynamic spatial audio objects that will be available to the stream after <i>hnsComplianceDeadlineTime</i>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



A dynamic <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> is one that was activated by setting the <i>type</i> parameter to the  <a href="https://msdn.microsoft.com/1B99E7FB-0796-4902-9B00-470FD08F8AFA">ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject</a> method to <b>AudioObjectType_Dynamic</b>. The client has a limit of the maximum number of dynamic spatial audio objects that can be activated at one time. When the capacity of the audio rendering pipeline changes, the system will dynamically adjust the maximum number of concurrent dynamic spatial audio objects. Before doing so, the system will call <b>OnAvailableDynamicObjectCountChange</b> to notify clients of the resource limit change. 

Call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on an <b>ISpatialAudioObject</b> when it is no longer being used to free up the resource to create new dynamic spatial audio objects.




## -see-also




<a href="https://msdn.microsoft.com/3729D985-9040-43AD-A8B0-045509FE2F20">ISpatialAudioObjectRenderStreamNotify</a>
 

 

