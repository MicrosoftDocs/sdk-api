---
UID: NS:dbt._DEV_BROADCAST_PORT_A
title: DEV_BROADCAST_PORT_A (dbt.h)
description: Contains information about a modem, serial, or parallel port. (ANSI)
helpviewer_keywords: ["*PDEV_BROADCAST_PORT_A","DEV_BROADCAST_PORT","DEV_BROADCAST_PORT structure","DEV_BROADCAST_PORT_A","PDEV_BROADCAST_PORT","PDEV_BROADCAST_PORT structure pointer","_win32_dev_broadcast_port_str","base.dev_broadcast_port_str","dbt/DEV_BROADCAST_PORT","dbt/PDEV_BROADCAST_PORT"]
old-location: base\dev_broadcast_port_str.htm
tech.root: base
ms.assetid: b8789f1c-7d82-4637-bdb0-016a22b3bc8a
ms.date: 12/05/2018
ms.keywords: '*PDEV_BROADCAST_PORT_A, DEV_BROADCAST_PORT, DEV_BROADCAST_PORT structure, DEV_BROADCAST_PORT_A, PDEV_BROADCAST_PORT, PDEV_BROADCAST_PORT structure pointer, _win32_dev_broadcast_port_str, base.dev_broadcast_port_str, dbt/DEV_BROADCAST_PORT, dbt/PDEV_BROADCAST_PORT'
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
req.typenames: DEV_BROADCAST_PORT_A, *PDEV_BROADCAST_PORT_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DEV_BROADCAST_PORT_A
 - dbt/_DEV_BROADCAST_PORT_A
 - PDEV_BROADCAST_PORT_A
 - dbt/PDEV_BROADCAST_PORT_A
 - DEV_BROADCAST_PORT_A
 - dbt/DEV_BROADCAST_PORT_A
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
 - DEV_BROADCAST_PORT - dev_broadcast_port_a
---

# DEV_BROADCAST_PORT_A structure


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

<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_hdr">DEV_BROADCAST_HDR</a>



<a href="/windows/desktop/DevIO/device-management-structures">Device Management Structures</a>



<a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>

## -remarks

> [!NOTE]
> The dbt.h header defines DEV_BROADCAST_PORT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
