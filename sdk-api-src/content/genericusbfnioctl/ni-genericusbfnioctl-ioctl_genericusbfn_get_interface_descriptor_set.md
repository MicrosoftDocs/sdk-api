---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET
title: IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET (genericusbfnioctl.h)
description: This I/O control code (IOCTL) is sent by a user-mode service or application to get the entire interface descriptor set for a function on the device.This IOCTL request does not retrieve the interface descriptor set for the entire device.Universal Serial Bus (USB) interface descriptor set for a function on the device.
helpviewer_keywords: ["IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET","IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET control","IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET control code [Buses]","buses.ioctl_genericusbfn_get_interface_descriptor_set","genericusbfnioctl/IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET"]
old-location: buses\ioctl_genericusbfn_get_interface_descriptor_set.htm
tech.root: buses
ms.assetid: 35069739-1E73-4F60-A16C-26EFF5D33D55
ms.date: 12/05/2018
ms.keywords: IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET, IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET control, IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET control code [Buses], buses.ioctl_genericusbfn_get_interface_descriptor_set, genericusbfnioctl/IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET
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
 - IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET
 - genericusbfnioctl/IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET
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
 - IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET
---

# IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET IOCTL


## -description

This I/O control code (IOCTL) is sent by a user-mode service or application to get the entire Universal Serial Bus (USB) interface descriptor set for a function on the device.<div class="alert"><b>Note</b>  This IOCTL request does not retrieve the interface descriptor set for the entire device.</div>
<div> </div>

## -ioctlparameters

### -input-buffer

A pointer to a <a href="/windows-hardware/drivers/ddi/content/usbfnbase/ns-usbfnbase-_usbfn_interface_info">USBFN_INTERFACE_INFO</a> structure.

### -input-buffer-length

The size of a <a href="/windows-hardware/drivers/ddi/content/usbfnbase/ns-usbfnbase-_usbfn_interface_info">USBFN_INTERFACE_INFO</a> structure.

### -output-buffer

A pointer to a buffer that contains a <a href="/windows-hardware/drivers/ddi/content/usbfnbase/ns-usbfnbase-_usbfn_interface_info">USBFN_INTERFACE_INFO</a> structure. The USB function class extension (UFX) populates the structure with the entire interface descriptor set including its endpoint descriptors.

### -output-buffer-length

The size of a <a href="/windows-hardware/drivers/ddi/content/usbfnbase/ns-usbfnbase-_usbfn_interface_info">USBFN_INTERFACE_INFO</a>.

### -in-out-buffer


### -inout-buffer-length


### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="/windows-hardware/drivers/kernel/ntstatus-values">NTSTATUS</a> code.

## -remarks

This request must be sent after sending the <a href="/windows/desktop/api/genericusbfnioctl/ni-genericusbfnioctl-ioctl_genericusbfn_activate_usb_bus">IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS</a> request.

The length of the entire interface descriptor is variable. The class driver might need to send this IOCTL request twice to get the entire descriptor set.

If the length of the entire descriptor set is greater than the  specified output buffer length, UFX sets the <b>Size</b> member of <a href="/windows-hardware/drivers/ddi/content/usbfnbase/ns-usbfnbase-_usbfn_interface_info">USBFN_INTERFACE_INFO</a> to the actual buffer length and fails the request with STATUS_BUFFER_TOO_SMALL. The driver must then allocated an output buffer of length specified by <b>Size</b> and resend the request. 

If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.

## -see-also

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>