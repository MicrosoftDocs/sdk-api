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

# BatteryClassIoctl function


## -description


<b>BatteryClassIoctl</b> handles system-defined battery IOCTLs.


## -parameters




### -param ClassData [in]

Pointer to a battery class handle that was previously returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff536266">BatteryClassInitializeDevice</a>.


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
The standard battery IOCTLs correspond to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536286">battery miniclass driver routines</a> (BatteryMini<i>Xxx</i> routines). 

When the miniclass driver is called with an <a href="https://msdn.microsoft.com/library/windows/hardware/ff548649">IRP_MJ_DEVICE_CONTROL</a> request, it should determine whether the IRP contains any private IOCTL defined by the miniclass driver. If so, the miniclass driver should satisfy the request, complete the IRP, and return.

If the IRP contains a public IOCTL, the driver should pass the IRP to the class driver's <b>BatteryClassIoctl</b> routine. This routine examines the IRP, determines whether it applies to the caller's battery device, and if so, calls the appropriate <a href="https://msdn.microsoft.com/de362d42-0185-4519-a5a6-b16e76d4dc4c">BatteryMiniXxx</a> routine to perform the requested operation. 

If <b>BatteryClassIoctl</b> returns STATUS_NOT_SUPPORTED for the IRP, the miniclass driver must either complete the IRP or forward it to the next-lower driver.




## -see-also




<a href="https://msdn.microsoft.com/bd96b79a-5670-4aaf-b72c-619818c2a2e7">BatteryMiniQueryInformation</a>



<a href="https://msdn.microsoft.com/04811f63-8a57-4b39-84c5-c9b7f803c057">BatteryMiniQueryStatus</a>



<a href="https://msdn.microsoft.com/030b7f5f-8ace-4dfc-8330-97aace86a1eb">BatteryMiniQueryTag</a>



<a href="https://msdn.microsoft.com/ebfcabb7-7447-486d-b980-7cb5456332f4">BatteryMiniSetInformation</a>
 

 

