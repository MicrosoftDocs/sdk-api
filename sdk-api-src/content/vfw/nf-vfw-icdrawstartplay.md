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

# ICDrawStartPlay macro


## -description



The <b>ICDrawStartPlay</b> macro provides the start and end times of a play operation to a rendering driver. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/27c4c06e-6510-43dc-a754-fe44144796f5">ICM_DRAW_START_PLAY</a> message.




## -parameters




### -param hic

Handle to a driver. 


### -param lFrom

Start time. 


### -param lTo

End time. 


## -remarks



This message precedes any frame data sent to the rendering driver.

Units for <i>lFrom</i> and <i>lTo</i> are specified with the <a href="https://msdn.microsoft.com/e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8">ICM_DRAW_BEGIN</a> message. For video data this is normally a frame number. For more information about the playback rate, see the <b>dwRate</b> and <b>dwScale</b> members of the <a href="https://msdn.microsoft.com/1ec2309c-7ea8-423e-aee3-5e0c650f0b3d">ICDRAWBEGIN</a> structure.

If the end time is less than the start time, the playback direction is reversed.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

