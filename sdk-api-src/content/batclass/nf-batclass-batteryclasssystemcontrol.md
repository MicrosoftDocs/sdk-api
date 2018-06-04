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

# BatteryClassSystemControl function


## -description


The <b>BatteryClassSystemControl</b> routine processes WMI IRPs on behalf of a battery miniclass driver.


## -parameters




### -param ClassData [in]

Pointer to a battery class handle that was previously received from <a href="https://msdn.microsoft.com/library/windows/hardware/ff536266">BatteryClassInitializeDevice</a>.


### -param WmiLibContext [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565813">WMILIB_CONTEXT</a> structure.  The structure provides WMI registration information, and dispatch routines for driver-specific WMI request processing.


### -param DeviceObject [in]

Pointer to the driver's device object.


### -param Irp [in, out]

Pointer to the IRP that contains the WMI request.


### -param Disposition [out]

Pointer to a memory location that the routine uses to return information about how it handled the IRP.  See <a href="https://msdn.microsoft.com/library/windows/hardware/ff565834">WmiSystemControl</a> for a description of the possible values returned.


## -returns



<b>BatteryClassSystemControl</b> returns STATUS_SUCCESS on success, and the appropriate error code on failure.




## -remarks



Battery miniclass drivers must call this routine instead of <a href="https://msdn.microsoft.com/library/windows/hardware/ff565834">WmiSystemControl</a>.  It provides the same functionality as <b>WmiSystemControl</b>, but it also ensures that the driver registers the WMI classes that the battery class driver handles on behalf of the miniclass driver.

A battery miniclass driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff544096">DpWmiQueryDataBlock</a> routine, which is specified by the <b>QueryWmiDataBlock</b> member of <a href="https://msdn.microsoft.com/library/windows/hardware/ff565813">WMILIB_CONTEXT</a>, must call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536268">BatteryClassQueryWmiDataBlock</a> routine to allow the battery class driver to process the query for the WMI classes it handles on behalf of the miniclass driver.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536268">BatteryClassQueryWmiDataBlock</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544096">DpWmiQueryDataBlock</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565813">WMILIB_CONTEXT</a>
 

 

