---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS
title: IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS (genericusbfnioctl.h)
description: This IOCTL code is nevtot supported.
helpviewer_keywords: ["IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS","IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS control","IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS control code [Buses]","buses.ioctl_genericusbfn_deactivate_usb_bus","genericusbfnioctl/IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS"]
old-location: buses\ioctl_genericusbfn_deactivate_usb_bus.htm
tech.root: buses
ms.assetid: 07F56732-590F-42B8-9939-5E02ED2A3EF0
ms.date: 12/05/2018
ms.keywords: IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS, IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS control, IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS control code [Buses], buses.ioctl_genericusbfn_deactivate_usb_bus, genericusbfnioctl/IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS
f1_keywords:
- genericusbfnioctl/IOCTL_GENERICUSBFN_DEACTIVATE_USB_BUS
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values">NTSTATUS</a> code. 


## -remarks



If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/genericusbfnioctl/ni-genericusbfnioctl-ioctl_genericusbfn_activate_usb_bus">IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS</a>
 

 

