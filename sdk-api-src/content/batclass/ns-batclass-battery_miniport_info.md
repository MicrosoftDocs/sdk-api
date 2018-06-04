---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# BATTERY_MINIPORT_INFO structure


## -description


Battery miniclass drivers fill in this structure before calling the battery class driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff536266">BatteryClassInitializeDevice</a> routine.


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

Pointer to the PDO for the battery device.


### -field DeviceName

Pointer to a Unicode string; should be NULL.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536266">BatteryClassInitializeDevice</a>
 

 

