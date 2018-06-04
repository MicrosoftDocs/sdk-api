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

# _DEV_BROADCAST_PORT_A structure


## -description


Contains information about a modem, serial, or parallel port.


## -struct-fields




### -field dbcp_size

The size of this structure, in bytes. This is the size of the members plus the actual length of the 
      <b>dbcp_name</b> string (the null character is accounted for by the declaration of 
      <b>dbcp_name</b> as a one-character array.)


### -field dbcp_devicetype

Set to <b>DBT_DEVTYP_PORT</b>.


### -field dbcp_reserved

Reserved; do not use.


### -field dbcp_name

A null-terminated string specifying the friendly name of the port or the device connected to the port. 
      Friendly names are intended to help the user quickly and accurately identify the device—for example, 
      "COM1" and "Standard 28800 bps Modem" are considered friendly names.


## -see-also




<a href="https://msdn.microsoft.com/4fc81fcb-b9fe-4016-b639-a43845af2c5f">DEV_BROADCAST_HDR</a>



<a href="https://msdn.microsoft.com/85ebbdca-94a0-4467-8d15-ee3a850e1cd9">Device Management Structures</a>



<a href="https://msdn.microsoft.com/b64a3983-ee75-4199-9778-1e5b7cec59e4">WM_DEVICECHANGE</a>
 

 

