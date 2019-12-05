---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_REGISTER_USB_STRING
title: IOCTL_GENERICUSBFN_REGISTER_USB_STRING (genericusbfnioctl.h)
description: This I/O control code (IOCTL) is sent by a user-mode service or application to register a string descriptor.Universal Serial Bus (USB) string descriptor.
old-location: buses\ioctl_genericusbfn_register_usb_string.htm
tech.root: usbref
ms.assetid: E3BDD2EF-C3F2-435E-8473-84C8FFAEAB06
ms.date: 12/05/2018
ms.keywords: IOCTL_GENERICUSBFN_REGISTER_USB_STRING, IOCTL_GENERICUSBFN_REGISTER_USB_STRING control, IOCTL_GENERICUSBFN_REGISTER_USB_STRING control code [Buses], buses.ioctl_genericusbfn_register_usb_string, genericusbfnioctl/IOCTL_GENERICUSBFN_REGISTER_USB_STRING
ms.topic: ioctl
f1_keywords:
- genericusbfnioctl/IOCTL_GENERICUSBFN_REGISTER_USB_STRING
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
- IOCTL_GENERICUSBFN_REGISTER_USB_STRING
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCTL_GENERICUSBFN_REGISTER_USB_STRING IOCTL


## -description



This I/O control code (IOCTL) is sent by a user-mode service or application to register a Universal Serial Bus (USB) string descriptor.




## -ioctlparameters




### -input-buffer

A pointer to a buffer that contains a  <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/usbfnbase/ns-usbfnbase-_usbfn_usb_string">USBFN_USB_STRING</a> structure with the USB string descriptor.


### -input-buffer-length

The size of a <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/usbfnbase/ns-usbfnbase-_usbfn_usb_string">USBFN_USB_STRING</a> structure.


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



This request must be sent after sending the <a href="https://docs.microsoft.com/windows/desktop/api/genericusbfnioctl/ni-genericusbfnioctl-ioctl_genericusbfn_activate_usb_bus">IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS</a> request.

If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>
 

 

