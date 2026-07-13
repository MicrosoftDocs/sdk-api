---
UID: NI:usbuser.IOCTL_USB_DIAGNOSTIC_MODE_ON
title: IOCTL_USB_DIAGNOSTIC_MODE_ON (usbuser.h)
description: The IOCTL_USB_DIAGNOSTIC_MODE_ON I/O control has been deprecated. Do not use.
helpviewer_keywords: ["IOCTL_USB_DIAGNOSTIC_MODE_ON","IOCTL_USB_DIAGNOSTIC_MODE_ON control","IOCTL_USB_DIAGNOSTIC_MODE_ON control code [Buses]","buses.ioctl_usb_diagnostic_mode_on","usbirp_c1493559-ce0a-4b79-8c7b-5fff2f3c83b3.xml","usbuser/IOCTL_USB_DIAGNOSTIC_MODE_ON"]
old-location: buses\ioctl_usb_diagnostic_mode_on.htm
tech.root: buses
ms.assetid: 9b3b7d11-a91c-4905-b639-d9843f05d65e
ms.date: 12/05/2018
ms.keywords: IOCTL_USB_DIAGNOSTIC_MODE_ON, IOCTL_USB_DIAGNOSTIC_MODE_ON control, IOCTL_USB_DIAGNOSTIC_MODE_ON control code [Buses], buses.ioctl_usb_diagnostic_mode_on, usbirp_c1493559-ce0a-4b79-8c7b-5fff2f3c83b3.xml, usbuser/IOCTL_USB_DIAGNOSTIC_MODE_ON
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
 - IOCTL_USB_DIAGNOSTIC_MODE_ON
 - usbuser/IOCTL_USB_DIAGNOSTIC_MODE_ON
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
 - IOCTL_USB_DIAGNOSTIC_MODE_ON
---

# IOCTL_USB_DIAGNOSTIC_MODE_ON IOCTL


## -description

The <b>IOCTL_USB_DIAGNOSTIC_MODE_ON</b> I/O control has been deprecated. Do not use.

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