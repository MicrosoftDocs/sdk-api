---
UID: NF:batclass.BatteryClassSystemControl
title: BatteryClassSystemControl function
author: windows-sdk-content
description: The BatteryClassSystemControl routine processes WMI IRPs on behalf of a battery miniclass driver.
old-location: battery\batteryclasssystemcontrol.htm
tech.root: battery
ms.assetid: d462c51d-e175-4fc8-88b9-515ba648fab4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BatteryClassSystemControl, BatteryClassSystemControl routine [Battery Devices], bat-rtn_4e2bda63-ff7a-420f-96af-fa0d5041479b.xml, batclass/BatteryClassSystemControl, battery.batteryclasssystemcontrol
ms.topic: function
req.header: batclass.h
req.include-header: Batclass.h
req.target-type: Desktop
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
req.lib: Battc.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Battc.lib
 - Battc.dll
api_name:
 - BatteryClassSystemControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BatteryClassSystemControl function


## -description


The <b>BatteryClassSystemControl</b> routine processes WMI IRPs on behalf of a battery miniclass driver.


## -parameters




### -param ClassData [in]

Pointer to a battery class handle that was previously received from <a href="https://msdn.microsoft.com/0af685a5-f5c2-4448-b8b2-f5cd9ed77047">BatteryClassInitializeDevice</a>.


### -param WmiLibContext [in]

Pointer to a <a href="https://msdn.microsoft.com/c9319f35-9745-47c4-a98d-4321e0d39f86">WMILIB_CONTEXT</a> structure.  The structure provides WMI registration information, and dispatch routines for driver-specific WMI request processing.


### -param DeviceObject [in]

Pointer to the driver's device object.


### -param Irp [in, out]

Pointer to the IRP that contains the WMI request.


### -param Disposition [out]

Pointer to a memory location that the routine uses to return information about how it handled the IRP.  See <a href="https://msdn.microsoft.com/6226e75e-b744-46cd-b14b-e93ece1c2f61">WmiSystemControl</a> for a description of the possible values returned.


## -returns



<b>BatteryClassSystemControl</b> returns STATUS_SUCCESS on success, and the appropriate error code on failure.




## -remarks



Battery miniclass drivers must call this routine instead of <a href="https://msdn.microsoft.com/6226e75e-b744-46cd-b14b-e93ece1c2f61">WmiSystemControl</a>.  It provides the same functionality as <b>WmiSystemControl</b>, but it also ensures that the driver registers the WMI classes that the battery class driver handles on behalf of the miniclass driver.

A battery miniclass driver's <a href="https://msdn.microsoft.com/c8996367-9ac5-4725-93ff-f13a334fbc5a">DpWmiQueryDataBlock</a> routine, which is specified by the <b>QueryWmiDataBlock</b> member of <a href="https://msdn.microsoft.com/c9319f35-9745-47c4-a98d-4321e0d39f86">WMILIB_CONTEXT</a>, must call the <a href="https://msdn.microsoft.com/2a5c4c14-fc80-4a0a-b447-6fe33ff1d42f">BatteryClassQueryWmiDataBlock</a> routine to allow the battery class driver to process the query for the WMI classes it handles on behalf of the miniclass driver.




## -see-also




<a href="https://msdn.microsoft.com/2a5c4c14-fc80-4a0a-b447-6fe33ff1d42f">BatteryClassQueryWmiDataBlock</a>



<a href="https://msdn.microsoft.com/c8996367-9ac5-4725-93ff-f13a334fbc5a">DpWmiQueryDataBlock</a>



<a href="https://msdn.microsoft.com/c9319f35-9745-47c4-a98d-4321e0d39f86">WMILIB_CONTEXT</a>
 

 

