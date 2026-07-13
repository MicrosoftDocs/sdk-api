---
UID: NI:usbuser.IOCTL_USB_GET_ROOT_HUB_NAME
title: IOCTL_USB_GET_ROOT_HUB_NAME (usbuser.h)
description: The IOCTL_USB_GET_ROOT_HUB_NAME I/O control request is used with the USB_ROOT_HUB_NAME structure to retrieve the symbolic link name of the root hub.IOCTL_USB_GET_ROOT_HUB_NAME is a user-mode I/O control request.
helpviewer_keywords: ["IOCTL_USB_GET_ROOT_HUB_NAME","IOCTL_USB_GET_ROOT_HUB_NAME control","IOCTL_USB_GET_ROOT_HUB_NAME control code [Buses]","buses.ioctl_usb_get_root_hub_name","usbirp_cf8d4d13-20cc-4134-8050-e3cd376a632e.xml","usbuser/IOCTL_USB_GET_ROOT_HUB_NAME"]
old-location: buses\ioctl_usb_get_root_hub_name.htm
tech.root: buses
ms.assetid: f1d7ab17-516a-4f6e-b343-3f67a6e07ae4
ms.date: 12/05/2018
ms.keywords: IOCTL_USB_GET_ROOT_HUB_NAME, IOCTL_USB_GET_ROOT_HUB_NAME control, IOCTL_USB_GET_ROOT_HUB_NAME control code [Buses], buses.ioctl_usb_get_root_hub_name, usbirp_cf8d4d13-20cc-4134-8050-e3cd376a632e.xml, usbuser/IOCTL_USB_GET_ROOT_HUB_NAME
req.header: usbuser.h
req.include-header: Usbioctl.h
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
 - IOCTL_USB_GET_ROOT_HUB_NAME
 - usbuser/IOCTL_USB_GET_ROOT_HUB_NAME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - usbuser.h
api_name:
 - IOCTL_USB_GET_ROOT_HUB_NAME
---

# IOCTL_USB_GET_ROOT_HUB_NAME IOCTL


## -description

The <b>IOCTL_USB_GET_ROOT_HUB_NAME</b> I/O control request is used with the <a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_root_hub_name">USB_ROOT_HUB_NAME</a> structure to retrieve the symbolic link name of the root hub.

<b>IOCTL_USB_GET_ROOT_HUB_NAME</b> is a user-mode I/O control request. This request targets the USB host controller (GUID_DEVINTERFACE_USB_HOST_CONTROLLER).

## -ioctlparameters

### -input-buffer

None.

### -input-buffer-length

None.

### -output-buffer

On output, the <b>AssociatedIrp.SystemBuffer</b> member points to a <a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_root_hub_name">USB_ROOT_HUB_NAME</a> structure that contains the symbolic link name of the root hub.  The leading "\xxx\ " text is not included in the retrieved string.

### -output-buffer-length

The size of a <a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_root_hub_name">USB_ROOT_HUB_NAME</a> structure.

### -in-out-buffer


### -inout-buffer-length


### -status-block

The USB stack sets <b>Irp-&gt;IoStatus.Status</b> to STATUS_SUCCESS if the request is successful. Otherwise, the USB stack sets <b>Status</b> to the appropriate error condition, such as STATUS_INVALID_PARAMETER or STATUS_INSUFFICIENT_RESOURCES.

If the root hub is removed or stopped, the request returns STATUS_SUCCESS but the string is NULL.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/usbioctl/ns-usbioctl-_usb_root_hub_name">USB_ROOT_HUB_NAME</a>