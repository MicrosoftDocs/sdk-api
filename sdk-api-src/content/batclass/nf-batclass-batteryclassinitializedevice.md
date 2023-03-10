---
UID: NF:batclass.BatteryClassInitializeDevice
title: BatteryClassInitializeDevice function (batclass.h)
description: The BatteryClassInitializeDevice routine initializes a new battery device for the class driver.
helpviewer_keywords: ["BatteryClassInitializeDevice","BatteryClassInitializeDevice routine [Battery Devices]","bat-rtn_19921d6e-cd86-40ad-86e3-acfc01fd8a56.xml","batclass/BatteryClassInitializeDevice","battery.batteryclassinitializedevice"]
old-location: battery\batteryclassinitializedevice.htm
tech.root: battery
ms.assetid: 0af685a5-f5c2-4448-b8b2-f5cd9ed77047
ms.date: 12/05/2018
ms.keywords: BatteryClassInitializeDevice, BatteryClassInitializeDevice routine [Battery Devices], bat-rtn_19921d6e-cd86-40ad-86e3-acfc01fd8a56.xml, batclass/BatteryClassInitializeDevice, battery.batteryclassinitializedevice
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BatteryClassInitializeDevice
 - batclass/BatteryClassInitializeDevice
dev_langs:
 - c++
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
---

# BatteryClassInitializeDevice function


## -description

The <b>BatteryClassInitializeDevice</b> routine initializes a new battery device for the class driver.

## -parameters

### -param MiniportInfo [in]

Pointer to a <a href="/windows/desktop/api/batclass/ns-batclass-battery_miniport_info">BATTERY_MINIPORT_INFO</a> structure.

### -param ClassData [out]

Pointer to a location at which <b>BatteryClassInitializeDevice</b> returns a handle to be used in subsequent calls to <a href="/windows-hardware/drivers/ddi/content/_battery/">BatteryMiniXxx</a> routines.

## -returns

<b>BatteryClassInitializeDevice</b> returns STATUS_SUCCESS or, possibly, STATUS_INSUFFICIENT_RESOURCES if not enough memory is available to store the battery miniclass data.

## -remarks

Battery miniclass drivers must call <b>BatteryClassInitializeDevice</b> to register each battery device and to pass data about the device and the miniclass driver to the battery class driver.

This routine should be called as part of the device initialization, typically from the miniclass driver's <a href="/windows-hardware/drivers/ddi/content/wdm/nc-wdm-driver_add_device">AddDevice</a> routine. 

The <b>Context</b> member of the <a href="/windows/desktop/api/batclass/ns-batclass-battery_miniport_info">BATTERY_MINIPORT_INFO</a> structure points to an area where the class and miniclass drivers maintain information about the battery device and its drivers. The context area typically contains the pageable device extension from the FDO and can also include other information at the discretion of the driver writer.

The class driver passes a pointer to the context area in calls to <a href="/windows-hardware/drivers/ddi/content/_battery/">battery miniclass driver routines</a> (BatteryMini<i>Xxx</i> routines). In their BatteryMini<i>Xxx</i> routines, miniclass drivers should read and write the device extension data through the passed-in pointer.

Miniclass drivers must use the <a href="/windows/desktop/api/batclass/ns-batclass-battery_miniport_info">BATTERY_MINIPORT_INFO</a> structure to supply entry points for all the <a href="/windows-hardware/drivers/ddi/content/_battery/">BatteryMiniXxx</a> routines.

If <b>BatteryClassInitializeDevice</b> successfully initializes the battery device, the caller is responsible for calling the <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassunload">BatteryClassUnload</a> function to free the resources for the battery device when it is no longer in use.

## -see-also

<a href="/windows/desktop/api/batclass/nf-batclass-batteryclassunload">BatteryClassUnload</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_disable_status_notify_callback">BatteryMiniDisableStatusNotify</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_query_information_callback">BatteryMiniQueryInformation</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_query_status_callback">BatteryMiniQueryStatus</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_query_tag_callback">BatteryMiniQueryTag</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_set_information_callback">BatteryMiniSetInformation</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_set_status_notify_callback">BatteryMiniSetStatusNotify</a>