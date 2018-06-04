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

# DCOMPOSITION_FRAME_STATISTICS structure


## -description


Describes timing and composition statistics for a frame.


## -struct-fields




### -field lastFrameTime

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

The time stamp of the last batch of commands to be processed by the composition engine.


### -field currentCompositionRate

Type: <b><a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a></b>

The rate at which the composition engine is producing frames, in frames per second.


### -field currentTime

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

The current time as computed by the <a href="https://msdn.microsoft.com/08169390-940b-4110-813a-249d107cc953">QueryPerformanceCounter</a> function.


### -field timeFrequency

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

The units in which the <b>lastFrameTime</b> and <b>currentTime</b> members are specified, in Hertz.


### -field nextEstimatedFrameTime

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

The estimated time when the next frame will be displayed.


## -remarks



The <a href="https://msdn.microsoft.com/C4DB7A16-BF91-4CD0-BCD2-4793D9599E0A">IDCompositionDevice::GetFrameStatistics</a> method fills this structure. An application can use the information in this structure to estimate the timestamp of the next few frames that will be started by the composition engine. Note that this is only an estimate because the composition engine may or may not compose the next frame, depending on whether any active animations or other work are pending for that frame. In addition, the composition engine may change frame rates according to the cost of composing individual frames.




## -see-also




<a href="https://msdn.microsoft.com/C4DB7A16-BF91-4CD0-BCD2-4793D9599E0A">IDCompositionDevice::GetFrameStatistics</a>
 

 

