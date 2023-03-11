---
UID: NS:batclass.BATTERY_MINIPORT_INFO
title: BATTERY_MINIPORT_INFO (batclass.h)
description: Battery miniclass drivers fill in this structure before calling the battery class driver's BatteryClassInitializeDevice routine.
helpviewer_keywords: ["*PBATTERY_MINIPORT_INFO","BATTERY_MINIPORT_INFO","BATTERY_MINIPORT_INFO structure [Battery Devices]","PBATTERY_MINIPORT_INFO","PBATTERY_MINIPORT_INFO structure pointer [Battery Devices]","bat-struct_0ef66c9a-61df-4c49-94f1-78e41e5b9bfb.xml","batclass/BATTERY_MINIPORT_INFO","batclass/PBATTERY_MINIPORT_INFO","battery.battery_miniport_info"]
old-location: battery\battery_miniport_info.htm
tech.root: battery
ms.assetid: db9d4e7d-a794-4c08-b849-d0b75ecf606b
ms.date: 12/05/2018
ms.keywords: '*PBATTERY_MINIPORT_INFO, BATTERY_MINIPORT_INFO, BATTERY_MINIPORT_INFO structure [Battery Devices], PBATTERY_MINIPORT_INFO, PBATTERY_MINIPORT_INFO structure pointer [Battery Devices], bat-struct_0ef66c9a-61df-4c49-94f1-78e41e5b9bfb.xml, batclass/BATTERY_MINIPORT_INFO, batclass/PBATTERY_MINIPORT_INFO, battery.battery_miniport_info'
req.header: batclass.h
req.include-header: Batclass.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BATTERY_MINIPORT_INFO, *PBATTERY_MINIPORT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PBATTERY_MINIPORT_INFO
 - batclass/PBATTERY_MINIPORT_INFO
 - BATTERY_MINIPORT_INFO
 - batclass/BATTERY_MINIPORT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - batclass.h
api_name:
 - BATTERY_MINIPORT_INFO
---

# BATTERY_MINIPORT_INFO structure


## -description

Battery miniclass drivers fill in this structure before calling the battery class driver's <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassinitializedevice">BatteryClassInitializeDevice</a> routine.

## -struct-fields

### -field MajorVersion

Specifies the major version number of the battery class driver. Miniclass drivers should specify BATTERY_CLASS_MAJOR_VERSION.

### -field MinorVersion

Specifies the minor version number of the battery class driver. Miniclass drivers should specify BATTERY_CLASS_MINOR_VERSION.

### -field Context

Pointer to the context area allocated by the miniclass driver.

### -field QueryTag

Specifies the entry point of the miniclass driver's <a href="/windows/desktop/api/batclass/nc-batclass-bclass_query_tag_callback">BatteryMiniQueryTag</a> routine.

### -field QueryInformation

Specifies the entry point of the miniclass driver's <a href="/windows/desktop/api/batclass/nc-batclass-bclass_query_information_callback">BatteryMiniQueryInformation</a> routine.

### -field SetInformation

Specifies the entry point of the miniclass driver's <a href="/windows/desktop/api/batclass/nc-batclass-bclass_set_information_callback">BatteryMiniSetInformation</a> routine.

### -field QueryStatus

Specifies the entry point of the miniclass driver's <a href="/windows/desktop/api/batclass/nc-batclass-bclass_query_status_callback">BatteryMiniQueryStatus</a> routine.

### -field SetStatusNotify

Specifies the entry point of the miniclass driver's <a href="/windows/desktop/api/batclass/nc-batclass-bclass_set_status_notify_callback">BatteryMiniSetStatusNotify</a> routine.

### -field DisableStatusNotify

Specifies the entry point of the miniclass driver's <a href="/windows/desktop/api/batclass/nc-batclass-bclass_disable_status_notify_callback">BatteryMiniDisableStatusNotify</a> routine.

### -field Pdo

Pointer to the PDO for the battery device.

### -field DeviceName

Pointer to a Unicode string; should be NULL.

## -see-also

<a href="/windows/desktop/api/batclass/nf-batclass-batteryclassinitializedevice">BatteryClassInitializeDevice</a>

