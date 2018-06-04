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

# _DEV_BROADCAST_HANDLE structure


## -description


Contains information about a file system handle.


## -struct-fields




### -field dbch_size

The size of this structure, in bytes.


### -field dbch_devicetype

Set to DBT_DEVTYP_HANDLE.


### -field dbch_reserved

Reserved; do not use.


### -field dbch_handle

A handle to the device to be checked.


### -field dbch_hdevnotify

A handle to the device notification. This handle is returned by 
<a href="https://msdn.microsoft.com/82094d95-9af3-4222-9c5e-ce2df9bab5e3">RegisterDeviceNotification</a>.


### -field dbch_eventguid

The GUID for the custom event. For more information, see 
<a href="https://msdn.microsoft.com/c89da4ac-57dd-4d95-ac86-3eb137dee0bc">Device Events</a>.  Valid only for <a href="https://msdn.microsoft.com/6e66fa93-0cd7-4202-83eb-cddc668525ae">DBT_CUSTOMEVENT</a>.


### -field dbch_nameoffset

The offset of an optional string buffer.  Valid only for <a href="https://msdn.microsoft.com/6e66fa93-0cd7-4202-83eb-cddc668525ae">DBT_CUSTOMEVENT</a>.


### -field dbch_data

Optional binary data.  This member is valid only for <a href="https://msdn.microsoft.com/6e66fa93-0cd7-4202-83eb-cddc668525ae">DBT_CUSTOMEVENT</a>.


## -see-also




<a href="https://msdn.microsoft.com/4fc81fcb-b9fe-4016-b639-a43845af2c5f">DEV_BROADCAST_HDR</a>



<a href="https://msdn.microsoft.com/b64a3983-ee75-4199-9778-1e5b7cec59e4">WM_DEVICECHANGE</a>
 

 

