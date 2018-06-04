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

# IWMVideoMediaProps::SetMaxKeyFrameSpacing


## -description



The <b>SetMaxKeyFrameSpacing</b> method specifies the maximum interval between key frames.




## -parameters




### -param llTime [in]

Maximum key-frame spacing in 100-nanosecond units.


## -returns



This method always returns S_OK.




## -remarks



A key frame is a video frame that can be rendered without any information being required from any previous frame. A delta frame is a frame that is dependent on a previous frame. The application can seek to a key frame, but not to a delta frame. The SDK does not enforce any limit on the time between key frames. In general, times longer than 30 seconds can adversely affect seek times both when the content is streamed over a network, and when it is played back locally. For recommended values, see <a href="https://msdn.microsoft.com/2df507f9-60a5-4489-b3db-7fe15604e625">Configuring Video Streams for Seeking Performance</a>.




## -see-also




<a href="https://msdn.microsoft.com/4d6ba1d8-b046-450b-a3f9-4810faba5b77">IWMVideoMediaProps Interface</a>



<a href="https://msdn.microsoft.com/125d352e-b181-4baa-8763-21315534beea">IWMVideoMediaProps::GetMaxKeyFrameSpacing</a>
 

 

