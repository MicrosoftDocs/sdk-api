---
UID: NF:batclass.BatteryClassInitializeDevice
title: BatteryClassInitializeDevice function
author: windows-sdk-content
description: The BatteryClassInitializeDevice routine initializes a new battery device for the class driver.
old-location: battery\batteryclassinitializedevice.htm
tech.root: battery
ms.assetid: 0af685a5-f5c2-4448-b8b2-f5cd9ed77047
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BatteryClassInitializeDevice, BatteryClassInitializeDevice routine [Battery Devices], bat-rtn_19921d6e-cd86-40ad-86e3-acfc01fd8a56.xml, batclass/BatteryClassInitializeDevice, battery.batteryclassinitializedevice
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - BatteryClassInitializeDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BatteryClassInitializeDevice function


## -description


The <b>BatteryClassInitializeDevice</b> routine initializes a new battery device for the class driver.


## -parameters




### -param MiniportInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Ff536287(v=VS.85).aspx">BATTERY_MINIPORT_INFO</a> structure.


### -param ClassData [out]

Pointer to a location at which <b>BatteryClassInitializeDevice</b> returns a handle to be used in subsequent calls to <a href="https://msdn.microsoft.com/en-us/library/Ff536286(v=VS.85).aspx">BatteryMiniXxx</a> routines.


## -returns



<b>BatteryClassInitializeDevice</b> returns STATUS_SUCCESS or, possibly, STATUS_INSUFFICIENT_RESOURCES if not enough memory is available to store the battery miniclass data.




## -remarks



Battery miniclass drivers must call <b>BatteryClassInitializeDevice</b> to register each battery device and to pass data about the device and the miniclass driver to the battery class driver.

This routine should be called as part of the device initialization, typically from the miniclass driver's <a href="https://msdn.microsoft.com/e6552c34-9310-4e26-9bcb-7b78d9e24480">AddDevice</a> routine. 

The <b>Context</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Ff536287(v=VS.85).aspx">BATTERY_MINIPORT_INFO</a> structure points to an area where the class and miniclass drivers maintain information about the battery device and its drivers. The context area typically contains the pageable device extension from the FDO and can also include other information at the discretion of the driver writer.

The class driver passes a pointer to the context area in calls to <a href="https://msdn.microsoft.com/en-us/library/Ff536286(v=VS.85).aspx">battery miniclass driver routines</a> (BatteryMini<i>Xxx</i> routines). In their BatteryMini<i>Xxx</i> routines, miniclass drivers should read and write the device extension data through the passed-in pointer.

Miniclass drivers must use the <a href="https://msdn.microsoft.com/en-us/library/Ff536287(v=VS.85).aspx">BATTERY_MINIPORT_INFO</a> structure to supply entry points for all the <a href="https://msdn.microsoft.com/en-us/library/Ff536286(v=VS.85).aspx">BatteryMiniXxx</a> routines.

If <b>BatteryClassInitializeDevice</b> successfully initializes the battery device, the caller is responsible for calling the <a href="https://msdn.microsoft.com/en-us/library/Ff536271(v=VS.85).aspx">BatteryClassUnload</a> function to free the resources for the battery device when it is no longer in use.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff536271(v=VS.85).aspx">BatteryClassUnload</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff536272(v=VS.85).aspx">BatteryMiniDisableStatusNotify</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff536273(v=VS.85).aspx">BatteryMiniQueryInformation</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff536274(v=VS.85).aspx">BatteryMiniQueryStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff536275(v=VS.85).aspx">BatteryMiniQueryTag</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff536276(v=VS.85).aspx">BatteryMiniSetInformation</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff536277(v=VS.85).aspx">BatteryMiniSetStatusNotify</a>
 

 

