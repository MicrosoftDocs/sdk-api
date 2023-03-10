---
UID: NS:batclass.BATTERY_MINIPORT_INFO_V1_1
title: BATTERY_MINIPORT_INFO_V1_1 (batclass.h)
description: Battery miniclass drivers fill in the BATTERY_MINIPORT_INFO_V1_1 structure before calling the battery class driver's BatteryClassInitializeDevice routine. BATTERY_MINIPORT_INFO_V1_1 is an updated version of the previous structure BATTERY_MINIPORT_INFO.
helpviewer_keywords: ["*PBATTERY_MINIPORT_INFO_V1_1","BATTERY_MINIPORT_INFO_V1_1","BATTERY_MINIPORT_INFO_V1_1 structure [Battery Devices]","PBATTERY_MINIPORT_INFO_V1_1","PBATTERY_MINIPORT_INFO_V1_1 structure pointer [Battery Devices]","batclass/BATTERY_MINIPORT_INFO_V1_1","batclass/PBATTERY_MINIPORT_INFO_V1_1","battery.battery_miniport_info_v1_1"]
old-location: battery\battery_miniport_info_v1_1.htm
tech.root: battery
ms.assetid: 3266126A-AEFC-445C-89D3-736545101522
ms.date: 12/05/2018
ms.keywords: '*PBATTERY_MINIPORT_INFO_V1_1, BATTERY_MINIPORT_INFO_V1_1, BATTERY_MINIPORT_INFO_V1_1 structure [Battery Devices], PBATTERY_MINIPORT_INFO_V1_1, PBATTERY_MINIPORT_INFO_V1_1 structure pointer [Battery Devices], batclass/BATTERY_MINIPORT_INFO_V1_1, batclass/PBATTERY_MINIPORT_INFO_V1_1, battery.battery_miniport_info_v1_1'
req.header: batclass.h
req.include-header: 
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
req.typenames: BATTERY_MINIPORT_INFO_V1_1, *PBATTERY_MINIPORT_INFO_V1_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PBATTERY_MINIPORT_INFO_V1_1
 - batclass/PBATTERY_MINIPORT_INFO_V1_1
 - BATTERY_MINIPORT_INFO_V1_1
 - batclass/BATTERY_MINIPORT_INFO_V1_1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Batclass.h
api_name:
 - BATTERY_MINIPORT_INFO_V1_1
---

# BATTERY_MINIPORT_INFO_V1_1 structure


## -description

Battery miniclass drivers fill in the <b>BATTERY_MINIPORT_INFO_V1_1</b> structure before calling the battery class driver's <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassinitializedevice">BatteryClassInitializeDevice</a> routine. <b>BATTERY_MINIPORT_INFO_V1_1</b> is an updated version of the previous structure <a href="/windows/desktop/api/batclass/ns-batclass-battery_miniport_info">BATTERY_MINIPORT_INFO</a>.

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

Pointer to the PDO (physical device object) for the battery device.

### -field DeviceName

Pointer to a Unicode string; should be NULL.

### -field Fdo

Pointer to the FDO (functional device object) for the battery device.

