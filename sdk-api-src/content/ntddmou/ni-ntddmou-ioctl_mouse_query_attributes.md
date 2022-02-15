---
UID: NI:ntddmou.IOCTL_MOUSE_QUERY_ATTRIBUTES
title: IOCTL_MOUSE_QUERY_ATTRIBUTES (ntddmou.h)
description: The IOCTL_MOUSE_QUERY_ATTRIBUTES request returns information about the mouse attributes.
helpviewer_keywords: ["IOCTL_MOUSE_QUERY_ATTRIBUTES","IOCTL_MOUSE_QUERY_ATTRIBUTES control","IOCTL_MOUSE_QUERY_ATTRIBUTES control code [Human Input Devices]","hid.ioctl_mouse_query_attributes","mref_078cb198-31ca-4b11-bc5b-33553bcb71a0.xml","ntddmou/IOCTL_MOUSE_QUERY_ATTRIBUTES"]
old-location: hid\ioctl_mouse_query_attributes.htm
tech.root: hid
ms.assetid: f5b82702-610a-41d3-96c9-2c4eae2244e3
ms.date: 12/05/2018
ms.keywords: IOCTL_MOUSE_QUERY_ATTRIBUTES, IOCTL_MOUSE_QUERY_ATTRIBUTES control, IOCTL_MOUSE_QUERY_ATTRIBUTES control code [Human Input Devices], hid.ioctl_mouse_query_attributes, mref_078cb198-31ca-4b11-bc5b-33553bcb71a0.xml, ntddmou/IOCTL_MOUSE_QUERY_ATTRIBUTES
req.header: ntddmou.h
req.include-header: Ntddmou.h
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
 - IOCTL_MOUSE_QUERY_ATTRIBUTES
 - ntddmou/IOCTL_MOUSE_QUERY_ATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddmou.h
api_name:
 - IOCTL_MOUSE_QUERY_ATTRIBUTES
---

# IOCTL_MOUSE_QUERY_ATTRIBUTES IOCTL


## -description

The IOCTL_MOUSE_QUERY_ATTRIBUTES request returns information about the mouse attributes.

Mouclass copies the current stack location, sets the <b>MajorFunction</b> member of the new stack location to <a href="/windows-hardware/drivers/kernel/irp-mj-internal-device-control">IRP_MJ_INTERNAL_DEVICE_CONTROL</a>, and sends this request down the device stack.

For more information about this request, see <a href="/windows-hardware/drivers/ddi/content/index">I8042prt Mouse Internal Device Control Requests</a>.

## -ioctlparameters

### -input-buffer

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to zero or a value greater than or equal to the size, in bytes, of a <a href="/windows/desktop/api/ntddmou/ns-ntddmou-mouse_unit_id_parameter">MOUSE_UNIT_ID_PARAMETER</a>. A value of zero specifies a default unit ID of zero.

The <b>AssociatedIrp.SystemBuffer </b> member points to a client-allocated buffer that is used to input and output information. On input, <b>AssociatedIrp.SystemBuffer</b> points to a MOUSE_UNIT_ID_PARAMETER structure. The client sets the <b>UnitId</b> member of the input structure.

The <b>Parameters.DeviceIoControl.OutputBufferLength</b> member specifies the size, in bytes, of an output buffer, which must be greater than or equal to the size in bytes of a <a href="/windows/desktop/api/ntddmou/ns-ntddmou-mouse_attributes">MOUSE_ATTRIBUTES</a> structure.

### -input-buffer-length

The size of a <a href="/windows/desktop/api/ntddmou/ns-ntddmou-mouse_unit_id_parameter">MOUSE_UNIT_ID_PARAMETER</a> structure.

### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to the client-allocated buffer that the lower-level drivers use to output a <a href="/windows/desktop/api/ntddmou/ns-ntddmou-mouse_attributes">MOUSE_ATTRIBUTES</a> structure.

### -output-buffer-length

The size of a <a href="/windows/desktop/api/ntddmou/ns-ntddmou-mouse_attributes">MOUSE_ATTRIBUTES</a> structure.

### -in-out-buffer


### -inout-buffer-length


### -status-block

The <b>Information</b> member is set to the number of bytes of attribute data that are returned if the request is successful. 

The <b>Status</b> member is set to one of the following values:

## -STATUS_BUFFER_TOO_SMALL

The <b>Parameters.DeviceIoControl.InputBufferLength </b> value is greater than zero but less than the size, in bytes, of a MOUSE_UNIT_ID_PARAMETER structure.

## -STATUS_INVALID_PARAMETER

The <b>UnitId </b> value is invalid.

## -STATUS_NOT_SUPPORTED

The target device is associated with a subordinate class device.

## -STATUS_SUCCESS

The request completed successfully.

## -see-also

<a href="/windows/desktop/api/ntddmou/ns-ntddmou-mouse_attributes">MOUSE_ATTRIBUTES</a>



<a href="/windows/desktop/api/ntddmou/ns-ntddmou-mouse_unit_id_parameter">MOUSE_UNIT_ID_PARAMETER</a>