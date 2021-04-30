---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_TRANSFER_OUT
title: IOCTL_GENERICUSBFN_TRANSFER_OUT (genericusbfnioctl.h)
description: This I/O control code (IOCTL) is sent by a user-mode service or application to issue an OUT direction transfer on the endpoint that corresponds to the specified pipe ID in the input buffer.
helpviewer_keywords: ["IOCTL_GENERICUSBFN_TRANSFER_OUT","IOCTL_GENERICUSBFN_TRANSFER_OUT control","IOCTL_GENERICUSBFN_TRANSFER_OUT control code [Buses]","buses.ioctl_genericusbfn_transfer_out","genericusbfnioctl/IOCTL_GENERICUSBFN_TRANSFER_OUT"]
old-location: buses\ioctl_genericusbfn_transfer_out.htm
tech.root: buses
ms.assetid: 4D0D546C-588F-4616-B9AA-9F811843EBE5
ms.date: 12/05/2018
ms.keywords: IOCTL_GENERICUSBFN_TRANSFER_OUT, IOCTL_GENERICUSBFN_TRANSFER_OUT control, IOCTL_GENERICUSBFN_TRANSFER_OUT control code [Buses], buses.ioctl_genericusbfn_transfer_out, genericusbfnioctl/IOCTL_GENERICUSBFN_TRANSFER_OUT
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
 - IOCTL_GENERICUSBFN_TRANSFER_OUT
 - genericusbfnioctl/IOCTL_GENERICUSBFN_TRANSFER_OUT
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
 - IOCTL_GENERICUSBFN_TRANSFER_OUT
---

# IOCTL_GENERICUSBFN_TRANSFER_OUT IOCTL


## -description

This  I/O control code (IOCTL) is sent by a user-mode service or application to issue an OUT direction transfer on the endpoint that corresponds to the specified pipe ID in the input buffer.

## -ioctlparameters

### -input-buffer

A <b>USBFNPIPEID</b> that specifies the ID of the pipe to conduct the transfer on.

### -input-buffer-length

The size of a <b>USBFNPIPEID</b>.

### -output-buffer

The data received from the host.

### -output-buffer-length

The size of the output buffer in bytes.

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



<a href="/windows/desktop/api/genericusbfnioctl/ni-genericusbfnioctl-ioctl_genericusbfn_transfer_in">IOCTL_GENERICUSBFN_TRANSFER_IN</a>



<a href="/windows/desktop/api/genericusbfnioctl/ni-genericusbfnioctl-ioctl_genericusbfn_transfer_in_append_zero_pkt">IOCTL_GENERICUSBFN_TRANSFER_IN_APPEND_ZERO_PKT</a>