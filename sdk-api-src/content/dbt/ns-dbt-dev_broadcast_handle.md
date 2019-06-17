---
UID: NS:dbt._DEV_BROADCAST_HANDLE
title: DEV_BROADCAST_HANDLE (dbt.h)
author: windows-sdk-content
description: Contains information about a file system handle.
old-location: base\dev_broadcast_handle_str.htm
tech.root: devio
ms.assetid: 5e542abc-8db3-4251-8b68-11456aa2da5e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDEV_BROADCAST_HANDLE, DEV_BROADCAST_HANDLE, DEV_BROADCAST_HANDLE structure, PDEV_BROADCAST_HANDLE, PDEV_BROADCAST_HANDLE structure pointer, _win32_dev_broadcast_handle_str, base.dev_broadcast_handle_str, dbt/DEV_BROADCAST_HANDLE, dbt/PDEV_BROADCAST_HANDLE"
ms.topic: struct
f1_keywords: ["dbt/DEV_BROADCAST_HANDLE"]
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
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a>.


### -field dbch_eventguid

The GUID for the custom event. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-events">Device Events</a>.  Valid only for <a href="https://docs.microsoft.com/windows/desktop/DevIO/dbt-customevent">DBT_CUSTOMEVENT</a>.


### -field dbch_nameoffset

The offset of an optional string buffer.  Valid only for <a href="https://docs.microsoft.com/windows/desktop/DevIO/dbt-customevent">DBT_CUSTOMEVENT</a>.


### -field dbch_data

Optional binary data.  This member is valid only for <a href="https://docs.microsoft.com/windows/desktop/DevIO/dbt-customevent">DBT_CUSTOMEVENT</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dbt/ns-dbt-_dev_broadcast_hdr">DEV_BROADCAST_HDR</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>
 

 

