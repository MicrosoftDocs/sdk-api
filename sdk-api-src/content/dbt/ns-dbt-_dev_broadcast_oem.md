---
UID: NS:dbt._DEV_BROADCAST_OEM
title: "_DEV_BROADCAST_OEM"
author: windows-sdk-content
description: Contains information about a OEM-defined device type.
old-location: base\dev_broadcast_oem_str.htm
tech.root: devio
ms.assetid: 32d72002-1e67-4f72-8821-6712eb898e7d
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: DEV_BROADCAST_OEM, DEV_BROADCAST_OEM structure, PDEV_BROADCAST_OEM, PDEV_BROADCAST_OEM structure pointer, _DEV_BROADCAST_OEM, _win32_dev_broadcast_oem_str, base.dev_broadcast_oem_str, dbt/DEV_BROADCAST_OEM, dbt/PDEV_BROADCAST_OEM
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
product: Windows
targetos: Windows
req.typenames: DEV_BROADCAST_OEM
req.redist: 
---

# _DEV_BROADCAST_OEM structure


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




<a href="https://msdn.microsoft.com/4fc81fcb-b9fe-4016-b639-a43845af2c5f">DEV_BROADCAST_HDR</a>



<a href="https://msdn.microsoft.com/b64a3983-ee75-4199-9778-1e5b7cec59e4">WM_DEVICECHANGE</a>
 

 

