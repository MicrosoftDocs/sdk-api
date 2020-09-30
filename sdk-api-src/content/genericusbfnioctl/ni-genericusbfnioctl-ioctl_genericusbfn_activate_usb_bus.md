---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS
title: IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS (genericusbfnioctl.h)
description: This I/O control code (IOCTL) is sent by a user-mode service or application to notify GenericUSBFn.sys to activate the Universal Serial Bus (USB). Once activated, the bus is prepared to process bus events and handle traffic.
helpviewer_keywords: ["IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS","IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS control","IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS control code [Buses]","buses.ioctl_genericusbfn_activate_usb_bus","genericusbfnioctl/IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS"]
old-location: buses\ioctl_genericusbfn_activate_usb_bus.htm
tech.root: buses
ms.assetid: A8CE2698-B2EF-409A-8251-7419F76D47BC
ms.date: 12/05/2018
ms.keywords: IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS, IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS control, IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS control code [Buses], buses.ioctl_genericusbfn_activate_usb_bus, genericusbfnioctl/IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS
 - genericusbfnioctl/IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - GenericUsbFnIoctl.h
api_name:
 - IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS
---

# IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS IOCTL


## -description

This I/O control code (IOCTL) is sent by a user-mode service or application to notify GenericUSBFn.sys  to activate the Universal Serial Bus (USB). Once activated, the bus is prepared to process bus events and handle traffic.

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

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="/windows-hardware/drivers/kernel/ntstatus-values">NTSTATUS</a> code.

## -remarks

If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.

## -see-also

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>