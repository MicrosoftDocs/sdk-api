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

# _USB_POWER_INFO structure


## -description


The <b>USB_POWER_INFO</b> structure is used with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve device power state that the host controller power policy specifies for the indicated system power state.


## -struct-fields




### -field SystemState

On input, a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540187">WDMUSB_POWER_STATE</a>-type enumerator value that specifies the system power state.


### -field HcDevicePowerState

On output, an <a href="https://msdn.microsoft.com/library/windows/hardware/ff540187">WDMUSB_POWER_STATE</a>-type enumerator value that specifies the device power state of the host controller.


### -field HcDeviceWake

On output, a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540187">WDMUSB_POWER_STATE</a>-type enumerator value that specifies whether the host controller is in a wake state.


### -field HcSystemWake

On output, a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540187">WDMUSB_POWER_STATE</a>-type enumerator value that specifies whether the host controller can wake the system.


### -field RhDevicePowerState

On output, a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540187">WDMUSB_POWER_STATE</a>-type enumerator value that specifies the device power state of the root hub.


### -field RhDeviceWake

On output, a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540187">WDMUSB_POWER_STATE</a>-type enumerator value that specifies whether the root hub is in a wake state.


### -field RhSystemWake

On output, a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540187">WDMUSB_POWER_STATE</a>-type enumerator value that specifies whether the root hub can wake the system.


### -field LastSystemSleepState

On output, a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540187">WDMUSB_POWER_STATE</a>-type enumerator value that specifies the last system sleep state.


### -field CanWakeup

A Boolean value that indicates whether the host controller device can wake up the system from the specified system power state. If <b>TRUE</b>, the host controller device can wake up the system. If <b>FALSE</b>, the host controller cannot wake up the system.


### -field IsPowered

A Boolean value that indicates whether the host controller is powered when in the specified system power state. If <b>TRUE</b>, the host controller is powered. If <b>FALSE</b>, the host controller is not powered.


## -remarks



The <b>USB_POWER_INFO</b> structure is used with the USBUSER_GET_POWER_STATE_MAP user-mode request. For more information about this request, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540160">USB Structures</a>
 

 

