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

# IMbnRegistrationEvents::OnRegisterStateChange


## -description


Notification method called by the Mobile Broadband service to indicate a change in the device's registration state.


## -parameters




### -param newInterface [in]

Pointer to an <a href="https://msdn.microsoft.com/da5413b7-adf4-4a3d-893f-f51441460541">IMbnRegistration</a> interface that represents the applicable device.


## -returns



This method must return <b>S_OK</b>.




## -remarks



The <b>OnRegisterStateChange</b> method is called by the Mobile Broadband service to signal a change in the device registration state. It may  be called if any of the following changes:

<ul>
<li>There is a change in the registration state of the device.  For example, if the device goes from its home network to a roaming network, then the registration state can change from <b>MBN_REGISTER_STATE_HOME</b> to <b>MBN_REGISTER_STATE_ROAMING</b>.</li>
<li>There is a change in registered provider ID, name, or roaming text.</li>
<li>There is a change in the last reported network error code for a registration operation.</li>
</ul>
An application can use the passed <a href="https://msdn.microsoft.com/da5413b7-adf4-4a3d-893f-f51441460541">IMbnRegistration</a> interface to get the updated registration state data.




## -see-also




<a href="https://msdn.microsoft.com/f3b60a93-3b57-4c2c-9114-912ca47f16b2">IMbnRegistrationEvents</a>
 

 

