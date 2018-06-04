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

# IWMStreamConfig::SetBufferWindow


## -description



The <b>SetBufferWindow</b> method specifies the maximum latency between when a stream is received and when it begins to be displayed.




## -parameters




### -param msBufferWindow [in]

Buffer window, in milliseconds.


## -returns



This method always returns S_OK.




## -remarks



For high bit rate streams (typically, more than 1 megabit per second), a latency (or buffer window) of 1 second is typical; for lower bit rate streams, a latency of approximately 3 seconds is often used.

Setting the buffer window to -1 (0xFFFFFFFF) indicates that the buffer window is unknown. In this case, the writer selects the buffer window size.

For video streams, a larger buffer window gives higher quality.

<div class="alert"><b>Note</b>  A problem can arise if you create a file containing streams with widely varying buffer windows. Playback applications created with a previous version of the Windows Media Format SDK have difficulty rendering the data from such files properly. If you are creating files to be used with older players, you should ensure that the buffer windows of any two streams do not vary by more than five seconds.</div>
<div> </div>
The new value will not take effect in the profile until you call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>



<a href="https://msdn.microsoft.com/7a78cd61-e7ae-42e2-9d64-f3344fefc59d">IWMStreamConfig::GetBufferWindow</a>
 

 

