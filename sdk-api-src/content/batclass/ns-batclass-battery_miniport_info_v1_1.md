---
UID: NS:batclass.BATTERY_MINIPORT_INFO_V1_1
title: BATTERY_MINIPORT_INFO_V1_1
author: windows-sdk-content
description: Battery miniclass drivers fill in the BATTERY_MINIPORT_INFO_V1_1 structure before calling the battery class driver's BatteryClassInitializeDevice routine. BATTERY_MINIPORT_INFO_V1_1 is an updated version of the previous structure BATTERY_MINIPORT_INFO.
old-location: battery\battery_miniport_info_v1_1.htm
tech.root: battery
ms.assetid: 3266126A-AEFC-445C-89D3-736545101522
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PBATTERY_MINIPORT_INFO_V1_1, BATTERY_MINIPORT_INFO_V1_1, BATTERY_MINIPORT_INFO_V1_1 structure [Battery Devices], PBATTERY_MINIPORT_INFO_V1_1, PBATTERY_MINIPORT_INFO_V1_1 structure pointer [Battery Devices], batclass/BATTERY_MINIPORT_INFO_V1_1, batclass/PBATTERY_MINIPORT_INFO_V1_1, battery.battery_miniport_info_v1_1"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Batclass.h
api_name:
 - BATTERY_MINIPORT_INFO_V1_1
product: Windows
targetos: Windows
req.typenames: BATTERY_MINIPORT_INFO_V1_1, *PBATTERY_MINIPORT_INFO_V1_1
req.redist: 
---

# BATTERY_MINIPORT_INFO_V1_1 structure


## -description


Battery miniclass drivers fill in the <b>BATTERY_MINIPORT_INFO_V1_1</b> structure before calling the battery class driver's <a href="https://msdn.microsoft.com/0af685a5-f5c2-4448-b8b2-f5cd9ed77047">BatteryClassInitializeDevice</a> routine. <b>BATTERY_MINIPORT_INFO_V1_1</b> is an updated version of the previous structure <a href="https://msdn.microsoft.com/db9d4e7d-a794-4c08-b849-d0b75ecf606b">BATTERY_MINIPORT_INFO</a>.


## -struct-fields




### -field MajorVersion

Specifies the major version number of the battery class driver. Miniclass drivers should specify BATTERY_CLASS_MAJOR_VERSION.


### -field MinorVersion

Specifies the minor version number of the battery class driver. Miniclass drivers should specify BATTERY_CLASS_MINOR_VERSION.


### -field Context

Pointer to the context area allocated by the miniclass driver. 


### -field QueryTag

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/030b7f5f-8ace-4dfc-8330-97aace86a1eb">BatteryMiniQueryTag</a> routine.


### -field QueryInformation

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/bd96b79a-5670-4aaf-b72c-619818c2a2e7">BatteryMiniQueryInformation</a> routine.


### -field SetInformation

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/ebfcabb7-7447-486d-b980-7cb5456332f4">BatteryMiniSetInformation</a> routine.


### -field QueryStatus

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/04811f63-8a57-4b39-84c5-c9b7f803c057">BatteryMiniQueryStatus</a> routine.


### -field SetStatusNotify

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/ec463202-4c08-475a-b612-73413f1376fc">BatteryMiniSetStatusNotify</a> routine.


### -field DisableStatusNotify

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/5120205f-0d55-4391-a560-3089fbe11d82">BatteryMiniDisableStatusNotify</a> routine.


### -field Pdo

Pointer to the PDO (physical device object) for the battery device.


### -field DeviceName

Pointer to a Unicode string; should be NULL.


### -field Fdo

Pointer to the FDO (functional device object) for the battery device.

