---
UID: NS:dbt._DEV_BROADCAST_HANDLE
title: DEV_BROADCAST_HANDLE
author: windows-sdk-content
description: Contains information about a file system handle.
old-location: base\dev_broadcast_handle_str.htm
tech.root: devio
ms.assetid: 5e542abc-8db3-4251-8b68-11456aa2da5e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDEV_BROADCAST_HANDLE, DEV_BROADCAST_HANDLE, DEV_BROADCAST_HANDLE structure, PDEV_BROADCAST_HANDLE, PDEV_BROADCAST_HANDLE structure pointer, _win32_dev_broadcast_handle_str, base.dev_broadcast_handle_str, dbt/DEV_BROADCAST_HANDLE, dbt/PDEV_BROADCAST_HANDLE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dbt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dbt.h
api_name:
 - DEV_BROADCAST_HANDLE
product: Windows
targetos: Windows
req.typenames: DEV_BROADCAST_HANDLE, *PDEV_BROADCAST_HANDLE
req.redist: 
---

# DEV_BROADCAST_HANDLE structure


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
 

 

