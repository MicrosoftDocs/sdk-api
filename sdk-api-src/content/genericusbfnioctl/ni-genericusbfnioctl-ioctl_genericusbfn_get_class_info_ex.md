---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX
title: IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX (genericusbfnioctl.h)
description: This I/O control code (IOCTL) is sent by a user-mode service or application to retrieve information about a device's available pipes as configured in the registry.
helpviewer_keywords: ["IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX","IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX control","IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX control code [Buses]","buses.ioctl_genericusbfn_get_class_info_ex","genericusbfnioctl/IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX"]
old-location: buses\ioctl_genericusbfn_get_class_info_ex.htm
tech.root: buses
ms.assetid: 9FC6E1F4-65AF-4315-B7F2-241E74820742
ms.date: 12/05/2018
ms.keywords: IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX, IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX control, IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX control code [Buses], buses.ioctl_genericusbfn_get_class_info_ex, genericusbfnioctl/IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX
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
 - IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX
 - genericusbfnioctl/IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX
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
 - IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX
---

# IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX IOCTL


## -description

This I/O control code (IOCTL) is sent by a  user-mode service or application to retrieve information about a device's available pipes as configured in the registry.

## -ioctlparameters

### -input-buffer

NULL.

### -input-buffer-length

None.

### -output-buffer

A <a href="/windows-hardware/drivers/ddi/content/usbfnbase/ns-usbfnbase-_usbfn_class_information_packet_ex">USBFN_CLASS_INFORMATION_PACKET_EX</a> that provides information about the available pipes for a device.

### -output-buffer-length

The size of a <a href="/windows-hardware/drivers/ddi/content/usbfnbase/ns-usbfnbase-_usbfn_class_information_packet_ex">USBFN_CLASS_INFORMATION_PACKET_EX</a> structure.

### -in-out-buffer


### -inout-buffer-length


### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="/windows-hardware/drivers/kernel/ntstatus-values">NTSTATUS</a> code.

## -remarks

If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.

## -see-also

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/genericusbfnioctl/ni-genericusbfnioctl-ioctl_genericusbfn_get_class_info">IOCTL_GENERICUSBFN_GET_CLASS_INFO</a>