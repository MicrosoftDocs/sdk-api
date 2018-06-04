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

# IMSVidStreamBufferSourceEvent3::BroadcastEvent


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>BroadcastEvent</b> method is called when the <a href="https://msdn.microsoft.com/4043e199-d329-45f3-80a7-cd84fad88979">MSVidStreamBufferSource</a> object receives a broadcast event through the <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a> interface.


## -parameters




### -param Guid [in]

GUID that specifies the event. For more information, see <a href="https://msdn.microsoft.com/974b42d7-bf68-426b-a146-4e520cac3274">IBroadcastEvent::Fire</a>.


## -returns



Return S_OK or an error code.




## -see-also




<a href="https://msdn.microsoft.com/4ff2e05f-1c26-48f2-8c46-beebb8b0b1b3">IMSVidStreamBufferSourceEvent3 Interface</a>
 

 

