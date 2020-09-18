---
UID: NF:batclass.BatteryClassIoctl
title: BatteryClassIoctl function (batclass.h)
description: BatteryClassIoctl handles system-defined battery IOCTLs.
helpviewer_keywords: ["BatteryClassIoctl","BatteryClassIoctl function [Battery Devices]","bat-rtn_bb0fcbcf-a26f-4f06-9f28-40bdc55b9d61.xml","batclass/BatteryClassIoctl","battery.batteryclassioctl"]
old-location: battery\batteryclassioctl.htm
tech.root: battery
ms.assetid: 8208552a-42a3-414f-849c-2bb0086c9f80
ms.date: 12/05/2018
ms.keywords: BatteryClassIoctl, BatteryClassIoctl function [Battery Devices], bat-rtn_bb0fcbcf-a26f-4f06-9f28-40bdc55b9d61.xml, batclass/BatteryClassIoctl, battery.batteryclassioctl
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
 - BatteryClassIoctl
 - batclass/BatteryClassIoctl
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
 - BatteryClassIoctl
---

# BatteryClassIoctl function


## -description

<b>BatteryClassIoctl</b> handles system-defined battery IOCTLs.

## -parameters

### -param ClassData [in]

Pointer to a battery class handle that was previously returned by <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassinitializedevice">BatteryClassInitializeDevice</a>.

### -param Irp [in, out]

Pointer to the IRP containing the IOCTL to be handled.

## -returns

<b>BatteryClassIoctl</b> returns STATUS_SUCCESS when it satisfies the request and completes the IRP. It returns STATUS_NOT_SUPPORTED for all IRPs other than device control IRPs that specify battery IOCTLs.

## -remarks

<b>BatteryClassIoctl</b> handles and completes device control IRPs intended for the battery. Such IRPs have one of the following I/O control codes: 

<ul>
<li>
IOCTL_BATTERY_QUERY_INFORMATION 

</li>
<li>
IOCTL_BATTERY_QUERY_STATUS

</li>
<li>
IOCTL_BATTERY_QUERY_TAG 

</li>
<li>
IOCTL_BATTERY_SET_INFORMATION

</li>
</ul>
The standard battery IOCTLs correspond to <a href="/windows-hardware/drivers/ddi/content/_battery/">battery miniclass driver routines</a> (BatteryMini<i>Xxx</i> routines). 

When the miniclass driver is called with an <a href="/windows-hardware/drivers/kernel/irp-mj-device-control">IRP_MJ_DEVICE_CONTROL</a> request, it should determine whether the IRP contains any private IOCTL defined by the miniclass driver. If so, the miniclass driver should satisfy the request, complete the IRP, and return.

If the IRP contains a public IOCTL, the driver should pass the IRP to the class driver's <b>BatteryClassIoctl</b> routine. This routine examines the IRP, determines whether it applies to the caller's battery device, and if so, calls the appropriate <a href="/windows-hardware/drivers/ddi/content/_battery/">BatteryMiniXxx</a> routine to perform the requested operation. 

If <b>BatteryClassIoctl</b> returns STATUS_NOT_SUPPORTED for the IRP, the miniclass driver must either complete the IRP or forward it to the next-lower driver.

## -see-also

<a href="/windows/desktop/api/batclass/nc-batclass-bclass_query_information_callback">BatteryMiniQueryInformation</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_query_status_callback">BatteryMiniQueryStatus</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_query_tag_callback">BatteryMiniQueryTag</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_set_information_callback">BatteryMiniSetInformation</a>