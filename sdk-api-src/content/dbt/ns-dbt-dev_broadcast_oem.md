---
UID: NS:dbt._DEV_BROADCAST_OEM
title: DEV_BROADCAST_OEM (dbt.h)

description: Contains information about a OEM-defined device type.
old-location: base\dev_broadcast_oem_str.htm
tech.root: devio
ms.assetid: 32d72002-1e67-4f72-8821-6712eb898e7d

ms.date: 12/05/2018
ms.keywords: DEV_BROADCAST_OEM, DEV_BROADCAST_OEM structure, PDEV_BROADCAST_OEM, PDEV_BROADCAST_OEM structure pointer, _win32_dev_broadcast_oem_str, base.dev_broadcast_oem_str, dbt/DEV_BROADCAST_OEM, dbt/PDEV_BROADCAST_OEM
ms.topic: struct
f1_keywords:
- dbt/DEV_BROADCAST_OEM
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
- DEV_BROADCAST_OEM
targetos: Windows
req.typenames: DEV_BROADCAST_OEM
req.redist: 
ms.custom: 19H1
---

# DEV_BROADCAST_OEM structure


## -description


Contains information about a OEM-defined device type.


## -struct-fields




### -field dbco_size

The size of this structure, in bytes.


### -field dbco_devicetype

Set to <b>DBT_DEVTYP_OEM</b>.


### -field dbco_reserved

Reserved; do not use.


### -field dbco_identifier

The OEM-specific identifier for the device.


### -field dbco_suppfunc

The OEM-specific function value. Possible values depend on the device.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dbt/ns-dbt-dev_broadcast_hdr">DEV_BROADCAST_HDR</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>
 

 

