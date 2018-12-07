---
UID: NS:batclass.__unnamed_struct_2
title: BATTERY_MINIPORT_INFO
author: windows-sdk-content
description: Battery miniclass drivers fill in this structure before calling the battery class driver's BatteryClassInitializeDevice routine.
old-location: battery\battery_miniport_info.htm
tech.root: battery
ms.assetid: db9d4e7d-a794-4c08-b849-d0b75ecf606b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PBATTERY_MINIPORT_INFO, BATTERY_MINIPORT_INFO, BATTERY_MINIPORT_INFO structure [Battery Devices], PBATTERY_MINIPORT_INFO, PBATTERY_MINIPORT_INFO structure pointer [Battery Devices], bat-struct_0ef66c9a-61df-4c49-94f1-78e41e5b9bfb.xml, batclass/BATTERY_MINIPORT_INFO, batclass/PBATTERY_MINIPORT_INFO, battery.battery_miniport_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - batclass.h
api_name:
 - BATTERY_MINIPORT_INFO
product: Windows
targetos: Windows
req.typenames: BATTERY_MINIPORT_INFO, *PBATTERY_MINIPORT_INFO
req.redist: 
---

# BATTERY_MINIPORT_INFO structure


## -description


Battery miniclass drivers fill in this structure before calling the battery class driver's <a href="https://msdn.microsoft.com/en-us/library/Ff536266(v=VS.85).aspx">BatteryClassInitializeDevice</a> routine.


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

Pointer to the PDO for the battery device.


### -field DeviceName

Pointer to a Unicode string; should be NULL.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff536266(v=VS.85).aspx">BatteryClassInitializeDevice</a>
 

 

