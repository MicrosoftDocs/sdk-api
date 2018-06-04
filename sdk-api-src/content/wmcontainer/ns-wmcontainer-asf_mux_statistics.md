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

# ASF_MUX_STATISTICS structure


## -description



Contains statistics about the progress of the ASF multiplexer.




## -struct-fields




### -field cFramesWritten

Number of frames written by the ASF multiplexer.


### -field cFramesDropped

Number of frames dropped by the ASF multiplexer.


## -remarks



Use <a href="https://msdn.microsoft.com/56083ceb-3d39-4fda-995a-f91fa0e16853">IMFASFMultiplexer::GetStatistics</a> to retrieve this structure.




## -see-also




<a href="https://msdn.microsoft.com/56083ceb-3d39-4fda-995a-f91fa0e16853">IMFASFMultiplexer::GetStatistics</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

