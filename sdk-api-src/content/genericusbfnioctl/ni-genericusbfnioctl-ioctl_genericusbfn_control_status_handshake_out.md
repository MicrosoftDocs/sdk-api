---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT
title: IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT (genericusbfnioctl.h)
description: This I/O control code (IOCTL) is sent by a user-mode service or application to complete a zero-length control status handshake on endpoint 0 in the OUT direction.helpviewer_keywords: ["IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT","IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT control","IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT control code [Buses]","buses.ioctl_genericusbfn_control_status_handshake_out","genericusbfnioctl/IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT"]
old-location: buses\ioctl_genericusbfn_control_status_handshake_out.htm
tech.root: usbref
ms.assetid: B8DE5F6E-6FC5-4E53-8A02-301A3CE436C9
ms.date: 12/05/2018
ms.keywords: IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT, IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT control, IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT control code [Buses], buses.ioctl_genericusbfn_control_status_handshake_out, genericusbfnioctl/IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT
f1_keywords:
- genericusbfnioctl/IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT
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
- IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT IOCTL


## -description



This   I/O control code (IOCTL) is sent by a user-mode service or application to complete  a zero-length control status handshake on endpoint 0 in the OUT direction.




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



<a href="https://docs.microsoft.com/windows/desktop/api/genericusbfnioctl/ni-genericusbfnioctl-ioctl_genericusbfn_control_status_handshake_in">IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN</a>
 

 

