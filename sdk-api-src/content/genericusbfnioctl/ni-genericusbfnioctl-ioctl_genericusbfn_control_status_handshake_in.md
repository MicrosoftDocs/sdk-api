---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN
title: IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN (genericusbfnioctl.h)
description: This I/O control code (IOCTL) is sent by a user mode service or application to request a zero-length control status handshake on endpoint 0 in the IN direction.
helpviewer_keywords: ["IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN","IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN control","IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN control code [Buses]","buses.ioctl_genericusbfn_control_status_handshake_in","genericusbfnioctl/IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN"]
old-location: buses\ioctl_genericusbfn_control_status_handshake_in.htm
tech.root: buses
ms.assetid: A01233F3-3C5F-4184-9AAA-7391BFD2EB02
ms.date: 12/05/2018
ms.keywords: IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN, IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN control, IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN control code [Buses], buses.ioctl_genericusbfn_control_status_handshake_in, genericusbfnioctl/IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN
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
 - IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN
 - genericusbfnioctl/IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN
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
 - IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN
---

# IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN IOCTL


## -description

This  I/O control code (IOCTL) is sent by a user mode service or application to request a zero-length control status handshake on endpoint 0 in the IN direction.

## -ioctlparameters

### -input-buffer

A <b>USBFNPIPEID</b> that specifies the pipe ID of endpoint 0.

### -input-buffer-length

The size of a <b>USBFNPIPEID</b>.

### -output-buffer

NULL.

### -output-buffer-length

None.

### -in-out-buffer


### -inout-buffer-length


### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="/windows-hardware/drivers/kernel/ntstatus-values">NTSTATUS</a> code.

## -remarks

If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.

## -see-also

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/genericusbfnioctl/ni-genericusbfnioctl-ioctl_genericusbfn_control_status_handshake_out">IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT</a>