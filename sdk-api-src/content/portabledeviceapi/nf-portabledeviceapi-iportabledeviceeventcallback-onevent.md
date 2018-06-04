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

# IPortableDeviceEventCallback::OnEvent


## -description



The <b>OnEvent</b> method is called by the SDK to notify the application about asynchronous events.




## -parameters




### -param pEventParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that contains event details.


## -returns



Any values returned by the application are ignored by Windows Portable Devices.




## -remarks



The application must register to receive events by calling <a href="https://msdn.microsoft.com/bab28a19-7ba2-4edd-b5aa-c2017b4bf8ca">IPortableDevice::Advise</a>.


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/529a8b7a-08b4-47de-8ed3-28e8fff0ede2">Handling Events from the Device</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/529a8b7a-08b4-47de-8ed3-28e8fff0ede2">Handling Events from the Device</a>



<a href="https://msdn.microsoft.com/1fb2d5d8-82b8-4c51-a086-bdcad33da190">IPortableDeviceEventCallback Interface</a>
 

 

