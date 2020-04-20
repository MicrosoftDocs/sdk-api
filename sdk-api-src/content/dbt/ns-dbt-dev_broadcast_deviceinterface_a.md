---
UID: NS:dbt._DEV_BROADCAST_DEVICEINTERFACE_A
title: DEV_BROADCAST_DEVICEINTERFACE_A (dbt.h)
description: Contains information about a class of devices.helpviewer_keywords: ["*PDEV_BROADCAST_DEVICEINTERFACE_A","DEV_BROADCAST_DEVICEINTERFACE","DEV_BROADCAST_DEVICEINTERFACE structure","DEV_BROADCAST_DEVICEINTERFACE_A","PDEV_BROADCAST_DEVICEINTERFACE","PDEV_BROADCAST_DEVICEINTERFACE structure pointer","_win32_dev_broadcast_deviceinterface_str","base.dev_broadcast_deviceinterface_str","dbt/DEV_BROADCAST_DEVICEINTERFACE","dbt/PDEV_BROADCAST_DEVICEINTERFACE"]
old-location: base\dev_broadcast_deviceinterface_str.htm
tech.root: devio
ms.assetid: 23e6b2b9-2053-4dfa-9c0a-283279f086b8
ms.date: 12/05/2018
ms.keywords: '*PDEV_BROADCAST_DEVICEINTERFACE_A, DEV_BROADCAST_DEVICEINTERFACE, DEV_BROADCAST_DEVICEINTERFACE structure, DEV_BROADCAST_DEVICEINTERFACE_A, PDEV_BROADCAST_DEVICEINTERFACE, PDEV_BROADCAST_DEVICEINTERFACE structure pointer, _win32_dev_broadcast_deviceinterface_str, base.dev_broadcast_deviceinterface_str, dbt/DEV_BROADCAST_DEVICEINTERFACE, dbt/PDEV_BROADCAST_DEVICEINTERFACE'
f1_keywords:
- dbt/DEV_BROADCAST_DEVICEINTERFACE
dev_langs:
- c++
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
- DEV_BROADCAST_DEVICEINTERFACE - dev_broadcast_deviceinterface_a
targetos: Windows
req.typenames: DEV_BROADCAST_DEVICEINTERFACE_A, *PDEV_BROADCAST_DEVICEINTERFACE_A
req.redist: 
ms.custom: 19H1
---

# DEV_BROADCAST_DEVICEINTERFACE_A structure


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
       <a href="https://docs.microsoft.com/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a> message, the 
       <b>dbcc_name</b> string is converted to ANSI as appropriate. Services always receive a 
       Unicode string, whether they call 
       <b>RegisterDeviceNotificationW</b> 
       or 
       <b>RegisterDeviceNotificationA</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dbt/ns-dbt-dev_broadcast_hdr">DEV_BROADCAST_HDR</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-structures">Device Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>
 

 

