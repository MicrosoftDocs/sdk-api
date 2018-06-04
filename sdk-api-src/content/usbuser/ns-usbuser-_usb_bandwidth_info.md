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

# _USB_BANDWIDTH_INFO structure


## -description


The <b>USB_BANDWIDTH_INFO</b> structure is used with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve information about the allocated bandwidth.


## -struct-fields




### -field DeviceCount

The number of devices on the bus.


### -field TotalBusBandwidth

The amount of allocated bandwidth, in bits per millisecond.


### -field Total32secBandwidth

The amount of allocated bandwidth bits in each 32-millisecond time slice.


### -field AllocedBulkAndControl

The amount of bandwidth, in bits per 32-millisecond, that is allocated for bulk and control transfers.


### -field AllocedIso

The amount of bandwidth, in bits per 32-millisecond, that is allocated for isochronous transfers.


### -field AllocedInterrupt_1ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 1 millisecond.


### -field AllocedInterrupt_2ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 2 milliseconds.


### -field AllocedInterrupt_4ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 4 milliseconds.


### -field AllocedInterrupt_8ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 8 milliseconds.


### -field AllocedInterrupt_16ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 16 milliseconds.


### -field AllocedInterrupt_32ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 32 milliseconds.


## -remarks



The <b>USB_BANDWIDTH_INFO</b> structure is used with the USBUSER_GET_BANDWIDTH_INFORMATION user-mode request. For a description of this request, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>.

In Windows 8, this request completes successfully. However, the values retrieved from the underlying USB 3.0 driver stack do not reflect actual information about the allocated bandwidth. That is because the bandwidth information is not exposed by xHCI controllers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540160">USB Structures</a>
 

 

