---
UID: NS:batclass.BATTERY_MINIPORT_INFO_V1_1
title: BATTERY_MINIPORT_INFO_V1_1
author: windows-sdk-content
description: Battery miniclass drivers fill in the BATTERY_MINIPORT_INFO_V1_1 structure before calling the battery class driver's BatteryClassInitializeDevice routine. BATTERY_MINIPORT_INFO_V1_1 is an updated version of the previous structure BATTERY_MINIPORT_INFO.
old-location: battery\battery_miniport_info_v1_1.htm
tech.root: battery
ms.assetid: 3266126A-AEFC-445C-89D3-736545101522
ms.author: windowssdkdev
ms.date: 07/30/2018
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


Battery miniclass drivers fill in the <b>BATTERY_MINIPORT_INFO_V1_1</b> structure before calling the battery class driver's <a href="https://msdn.microsoft.com/en-us/library/Ff536266(v=VS.85).aspx">BatteryClassInitializeDevice</a> routine. <b>BATTERY_MINIPORT_INFO_V1_1</b> is an updated version of the previous structure <a href="https://msdn.microsoft.com/en-us/library/Ff536287(v=VS.85).aspx">BATTERY_MINIPORT_INFO</a>.


## -struct-fields




### -field MajorVersion

Specifies the major version number of the battery class driver. Miniclass drivers should specify BATTERY_CLASS_MAJOR_VERSION.


### -field MinorVersion

Specifies the minor version number of the battery class driver. Miniclass drivers should specify BATTERY_CLASS_MINOR_VERSION.


### -field Context

Pointer to the context area allocated by the miniclass driver. 


### -field QueryTag

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/en-us/library/Ff536275(v=VS.85).aspx">BatteryMiniQueryTag</a> routine.


### -field QueryInformation

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/en-us/library/Ff536273(v=VS.85).aspx">BatteryMiniQueryInformation</a> routine.


### -field SetInformation

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/en-us/library/Ff536276(v=VS.85).aspx">BatteryMiniSetInformation</a> routine.


### -field QueryStatus

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/en-us/library/Ff536274(v=VS.85).aspx">BatteryMiniQueryStatus</a> routine.


### -field SetStatusNotify

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/en-us/library/Ff536277(v=VS.85).aspx">BatteryMiniSetStatusNotify</a> routine.


### -field DisableStatusNotify

Specifies the entry point of the miniclass driver's <a href="https://msdn.microsoft.com/en-us/library/Ff536272(v=VS.85).aspx">BatteryMiniDisableStatusNotify</a> routine.


### -field Pdo

Pointer to the PDO (physical device object) for the battery device.


### -field DeviceName

Pointer to a Unicode string; should be NULL.


### -field Fdo

Pointer to the FDO (functional device object) for the battery device.

