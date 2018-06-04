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

# IMbnDeviceServicesEvents::OnInterfaceStateChange


## -description


Notification method that signals a change in the state of device services on the system.


## -parameters




### -param interfaceID [in]

The <a href="https://msdn.microsoft.com/9828567b-ef5e-44b7-90ce-1788cd8dd947">InterfaceID</a> of the device for which the device services state change notification is sent.


### -param stateChange [in]

A <a href="https://msdn.microsoft.com/0EDED390-CB60-4D6C-9E62-87B3BF6F9050">MBN_DEVICE_SERVICES_INTERFACE_STATE</a> enumeration that specifies whether the device service capable device is available or unavailable.


## -returns



The method must return the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a>
 

 

