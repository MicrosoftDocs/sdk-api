---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS
title: IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS
author: windows-sdk-content
description: This IOCTL code is nevtot supported.
old-location: buses\ioctl_genericusbfn_deactivate_usb_bus.htm
tech.root: usbref
ms.assetid: 07F56732-590F-42B8-9939-5E02ED2A3EF0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS, IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS control, IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS control code [Buses], buses.ioctl_genericusbfn_deactivate_usb_bus, genericusbfnioctl/IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: genericusbfnioctl.h
req.include-header: GenericUsbFnIoctl.h
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
 - GenericUsbFnIoctl.h
api_name:
 - IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS IOCTL


## -description


This IOCTL code is nevtot supported.

This I/O control code (IOCTL) is sent by the user-mode service or application  this request to notify GenericUSBFn.sys to deactivate the Universal Serial Bus (USB). When deactivated, the bus can no longer process bus events and handle traffic. 


## -ioctlparameters




### -input-buffer

NULL.


### -input-buffer-length

None.


### -output-buffer

NULL.


### -output-buffer-length

None.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks



If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/A8CE2698-B2EF-409A-8251-7419F76D47BC">IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS</a>
 

 

