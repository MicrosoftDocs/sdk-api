---
UID: NS:dbt._DEV_BROADCAST_DEVICEINTERFACE_W
title: DEV_BROADCAST_DEVICEINTERFACE_W (dbt.h)
description: Contains information about a class of devices. (Unicode)
helpviewer_keywords: ["*PDEV_BROADCAST_DEVICEINTERFACE_W","DEV_BROADCAST_DEVICEINTERFACE","DEV_BROADCAST_DEVICEINTERFACE structure","DEV_BROADCAST_DEVICEINTERFACE_W","PDEV_BROADCAST_DEVICEINTERFACE","PDEV_BROADCAST_DEVICEINTERFACE structure pointer","_win32_dev_broadcast_deviceinterface_str","base.dev_broadcast_deviceinterface_str","dbt/DEV_BROADCAST_DEVICEINTERFACE","dbt/PDEV_BROADCAST_DEVICEINTERFACE"]
old-location: base\dev_broadcast_deviceinterface_str.htm
tech.root: base
ms.assetid: 23e6b2b9-2053-4dfa-9c0a-283279f086b8
ms.date: 12/05/2018
ms.keywords: '*PDEV_BROADCAST_DEVICEINTERFACE_W, DEV_BROADCAST_DEVICEINTERFACE, DEV_BROADCAST_DEVICEINTERFACE structure, DEV_BROADCAST_DEVICEINTERFACE_W, PDEV_BROADCAST_DEVICEINTERFACE, PDEV_BROADCAST_DEVICEINTERFACE structure pointer, _win32_dev_broadcast_deviceinterface_str, base.dev_broadcast_deviceinterface_str, dbt/DEV_BROADCAST_DEVICEINTERFACE, dbt/PDEV_BROADCAST_DEVICEINTERFACE'
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
targetos: Windows
req.typenames: DEV_BROADCAST_DEVICEINTERFACE_W, *PDEV_BROADCAST_DEVICEINTERFACE_W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DEV_BROADCAST_DEVICEINTERFACE_W
 - dbt/_DEV_BROADCAST_DEVICEINTERFACE_W
 - PDEV_BROADCAST_DEVICEINTERFACE_W
 - dbt/PDEV_BROADCAST_DEVICEINTERFACE_W
 - DEV_BROADCAST_DEVICEINTERFACE_W
 - dbt/DEV_BROADCAST_DEVICEINTERFACE_W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dbt.h
api_name:
 - DEV_BROADCAST_DEVICEINTERFACE - dev_broadcast_deviceinterface_w
---

# DEV_BROADCAST_DEVICEINTERFACE_W structure


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
       <a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a> message, the 
       <b>dbcc_name</b> string is converted to ANSI as appropriate. Services always receive a 
       Unicode string, whether they call 
       <b>RegisterDeviceNotificationW</b> 
       or 
       <b>RegisterDeviceNotificationA</b>.

## -see-also

<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_hdr">DEV_BROADCAST_HDR</a>



<a href="/windows/desktop/DevIO/device-management-structures">Device Management Structures</a>



<a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a>



<a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>

## -remarks

> [!NOTE]
> The dbt.h header defines DEV_BROADCAST_DEVICEINTERFACE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
