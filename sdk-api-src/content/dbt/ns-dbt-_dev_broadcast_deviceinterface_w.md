---
UID: NS:dbt._DEV_BROADCAST_DEVICEINTERFACE_W
title: "_DEV_BROADCAST_DEVICEINTERFACE_W"
author: windows-sdk-content
description: Contains information about a class of devices.
old-location: base\dev_broadcast_deviceinterface_str.htm
old-project: devio
ms.assetid: 23e6b2b9-2053-4dfa-9c0a-283279f086b8
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*PDEV_BROADCAST_DEVICEINTERFACE_W, DEV_BROADCAST_DEVICEINTERFACE, DEV_BROADCAST_DEVICEINTERFACE structure, DEV_BROADCAST_DEVICEINTERFACE_W, PDEV_BROADCAST_DEVICEINTERFACE, PDEV_BROADCAST_DEVICEINTERFACE structure pointer, _DEV_BROADCAST_DEVICEINTERFACE_W, _win32_dev_broadcast_deviceinterface_str, base.dev_broadcast_deviceinterface_str, dbt/DEV_BROADCAST_DEVICEINTERFACE, dbt/PDEV_BROADCAST_DEVICEINTERFACE"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DEV_BROADCAST_DEVICEINTERFACE_W, *PDEV_BROADCAST_DEVICEINTERFACE_W
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dbt.h
api_name:
 - DEV_BROADCAST_DEVICEINTERFACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DEV_BROADCAST_DEVICEINTERFACE_W structure


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
 

 

