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

# ICGetBuffersWanted macro


## -description



The <b>ICGetBuffersWanted</b> macro queries a driver for the number of buffers to allocate. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/109e8627-7ed4-4f17-bf7f-e77f42dfc8c7">ICM_GETBUFFERSWANTED</a> message.




## -parameters




### -param hic

Handle to a driver. 


### -param lpdwBuffers

Address to contain the number of samples the driver needs to efficiently render the data. 


## -remarks



This message is used by drivers that use hardware to render data and want to ensure a minimal time lag caused by waiting for buffers to arrive. For example, if a driver controls a video decompression board that can hold 10 frames of video, it could return 10 for this message. This instructs applications to try to stay 10 frames ahead of the frame it currently needs.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

