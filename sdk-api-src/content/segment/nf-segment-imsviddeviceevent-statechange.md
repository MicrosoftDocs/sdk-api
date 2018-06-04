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

# IMSVidDeviceEvent::StateChange


## -description



This topic applies to Windows XP or later.
        



The <b>StateChange</b> method signals that the state of the device has changed.


## -parameters




### -param lpd




### -param oldState [in]

Specifies the old state as an <a href="https://msdn.microsoft.com/b4da9c6e-3235-4c78-b9e1-57c9d06fccbc">MSVidCtlStateList</a> value.


### -param newState [in]

Specifies the new state as an <a href="https://msdn.microsoft.com/b4da9c6e-3235-4c78-b9e1-57c9d06fccbc">MSVidCtlStateList</a> value.


#### - plpd [in]

Pointer to the device object that signaled the change.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The dispatch identifier (dispid) of this method is <b>eventidStateChange</b>.




## -see-also




<a href="https://msdn.microsoft.com/1a5a9bc1-7d18-4aa9-bc5f-318f7bedbc48">IMSVidDeviceEvent</a>
 

 

