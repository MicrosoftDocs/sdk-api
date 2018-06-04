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

# _DEV_BROADCAST_DEVICEINTERFACE_A structure


## -description


Contains information about a class of devices.


## -struct-fields




### -field dbcc_size

The size of this structure, in bytes. This is the size of the members plus the actual length of the 
      <b>dbcc_name</b> string (the null character is accounted for by the declaration of 
      <b>dbcc_name</b> as a one-character array.)


### -field dbcc_devicetype

Set to <b>DBT_DEVTYP_DEVICEINTERFACE</b>.


### -field dbcc_reserved

Reserved; do not use.


### -field dbcc_classguid

The GUID for the interface device class.


### -field dbcc_name

A null-terminated string that specifies the name of the device.

When this structure is returned to a window through the 
       <a href="https://msdn.microsoft.com/b64a3983-ee75-4199-9778-1e5b7cec59e4">WM_DEVICECHANGE</a> message, the 
       <b>dbcc_name</b> string is converted to ANSI as appropriate. Services always receive a 
       Unicode string, whether they call 
       <b>RegisterDeviceNotificationW</b> 
       or 
       <b>RegisterDeviceNotificationA</b>.


## -see-also




<a href="https://msdn.microsoft.com/4fc81fcb-b9fe-4016-b639-a43845af2c5f">DEV_BROADCAST_HDR</a>



<a href="https://msdn.microsoft.com/85ebbdca-94a0-4467-8d15-ee3a850e1cd9">Device Management Structures</a>



<a href="https://msdn.microsoft.com/82094d95-9af3-4222-9c5e-ce2df9bab5e3">RegisterDeviceNotification</a>



<a href="https://msdn.microsoft.com/b64a3983-ee75-4199-9778-1e5b7cec59e4">WM_DEVICECHANGE</a>
 

 

