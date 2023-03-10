---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_SET_PIPE_STATE
title: IOCTL_GENERICUSBFN_SET_PIPE_STATE (genericusbfnioctl.h)
description: This I/O control code (IOCTL) is sent by a user-mode service or application to set the state of the specified Universal Serial Bus (USB) pipe.
helpviewer_keywords: ["IOCTL_GENERICUSBFN_SET_PIPE_STATE","IOCTL_GENERICUSBFN_SET_PIPE_STATE control","IOCTL_GENERICUSBFN_SET_PIPE_STATE control code [Buses]","buses.ioctl_genericusbfn_set_pipe_state","genericusbfnioctl/IOCTL_GENERICUSBFN_SET_PIPE_STATE"]
old-location: buses\ioctl_genericusbfn_set_pipe_state.htm
tech.root: buses
ms.assetid: C9276A60-382C-40FE-B5B9-49E95C71CDE9
ms.date: 12/05/2018
ms.keywords: IOCTL_GENERICUSBFN_SET_PIPE_STATE, IOCTL_GENERICUSBFN_SET_PIPE_STATE control, IOCTL_GENERICUSBFN_SET_PIPE_STATE control code [Buses], buses.ioctl_genericusbfn_set_pipe_state, genericusbfnioctl/IOCTL_GENERICUSBFN_SET_PIPE_STATE
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
 - IOCTL_GENERICUSBFN_SET_PIPE_STATE
 - genericusbfnioctl/IOCTL_GENERICUSBFN_SET_PIPE_STATE
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
 - IOCTL_GENERICUSBFN_SET_PIPE_STATE
---

# IOCTL_GENERICUSBFN_SET_PIPE_STATE IOCTL


## -description

This I/O control code (IOCTL) is sent by a user-mode service or application to set the state of the specified Universal Serial Bus (USB) pipe.

## -ioctlparameters

### -input-buffer

A <b>USBFNPIPEID</b> that specifies the ID of the pipe to configure.

### -input-buffer-length

The size of a <b>USBFNPIPEID</b>.

### -output-buffer

Contains a boolean value that specifies whether the specified pipe is stalled. A value of TRUE if the specified pipe is stalled; FALSE if otherwise.

### -output-buffer-length

The size of the output buffer in bytes.

### -in-out-buffer


### -inout-buffer-length


### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="/windows-hardware/drivers/kernel/ntstatus-values">NTSTATUS</a> code.

## -remarks

The  pipe will send STALL transaction packets to the host when stalled. For more information, see the USB specification.

If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.

## -see-also

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/genericusbfnioctl/ni-genericusbfnioctl-ioctl_genericusbfn_get_pipe_state">IOCTL_GENERICUSBFN_GET_PIPE_STATE</a>