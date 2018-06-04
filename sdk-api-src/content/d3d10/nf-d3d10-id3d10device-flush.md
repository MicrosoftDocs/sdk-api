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

# ID3D10Device::Flush


## -description


Send queued-up commands in the command buffer to the GPU.


## -parameters






## -returns



Returns nothing.




## -remarks



Most applications will not need to call this method. Calling this method when not necessary will incur a performance penalty. Each call to <b>Flush</b> incurs a significant amount of overhead.

When Direct3D state-setting, present, or draw commands are called by an application, those commands are queued into an internal command buffer. <b>Flush</b> sends those commands to the GPU for processing. Normally, these commands are sent to the GPU automatically whenever Direct3D determines that they need to be, such as when the command buffer is full or when mapping a resource. <b>Flush</b> will send the commands manually.

<b>Flush</b> should be used when the CPU waits for an arbitrary amount of time (such as when calling <a href="http://msdn2.microsoft.com/en-us/library/ms686298.aspx">Sleep</a>, <a href="https://msdn.microsoft.com/d81c57d6-475c-444b-82c0-87b29ce0cbb4">ID3DX10ThreadPump::WaitForAllItems</a>, or <a href="https://msdn.microsoft.com/54b1dd37-65f2-40b2-9f6c-0ea00864e546">WaitForVBlank</a>.

For more information about how flushing works, see <a href="https://msdn.microsoft.com/f969be42-d541-4e8d-aec4-eb9508bcc7cf">Accurately Profiling Direct3D API Calls (Direct3D 9)</a>.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

