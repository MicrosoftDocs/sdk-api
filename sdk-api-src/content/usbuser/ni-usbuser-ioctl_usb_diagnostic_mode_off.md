---
UID: NI:usbuser.IOCTL_USB_DIAGNOSTIC_MODE_OFF
title: IOCTL_USB_DIAGNOSTIC_MODE_OFF (usbuser.h)
description: The IOCTL_USB_DIAGNOSTIC_MODE_OFF I/O control has been deprecated. Do not use.
helpviewer_keywords: ["IOCTL_USB_DIAGNOSTIC_MODE_OFF","IOCTL_USB_DIAGNOSTIC_MODE_OFF control","IOCTL_USB_DIAGNOSTIC_MODE_OFF control code [Buses]","buses.ioctl_usb_diagnostic_mode_off","usbirp_7b761254-b350-4ac8-820f-04426139f6bb.xml","usbuser/IOCTL_USB_DIAGNOSTIC_MODE_OFF"]
old-location: buses\ioctl_usb_diagnostic_mode_off.htm
tech.root: buses
ms.assetid: 8452c9a2-3e1f-4b62-8ab2-9071d55f5f68
ms.date: 12/05/2018
ms.keywords: IOCTL_USB_DIAGNOSTIC_MODE_OFF, IOCTL_USB_DIAGNOSTIC_MODE_OFF control, IOCTL_USB_DIAGNOSTIC_MODE_OFF control code [Buses], buses.ioctl_usb_diagnostic_mode_off, usbirp_7b761254-b350-4ac8-820f-04426139f6bb.xml, usbuser/IOCTL_USB_DIAGNOSTIC_MODE_OFF
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
 - IOCTL_USB_DIAGNOSTIC_MODE_OFF
 - usbuser/IOCTL_USB_DIAGNOSTIC_MODE_OFF
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
 - IOCTL_USB_DIAGNOSTIC_MODE_OFF
---

# IOCTL_USB_DIAGNOSTIC_MODE_OFF IOCTL


## -description

The <b>IOCTL_USB_DIAGNOSTIC_MODE_OFF</b> I/O control has been deprecated. Do not use.

## -ioctlparameters

### -input-buffer



### -input-buffer-length



### -output-buffer



### -output-buffer-length



### -in-out-buffer



### -inout-buffer-length



### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).