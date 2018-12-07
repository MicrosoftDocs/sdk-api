---
UID: NI:usbuser.IOCTL_USB_DIAGNOSTIC_MODE_ON
title: IOCTL_USB_DIAGNOSTIC_MODE_ON
author: windows-sdk-content
description: The IOCTL_USB_DIAGNOSTIC_MODE_ON I/O control has been deprecated. Do not use.
old-location: buses\ioctl_usb_diagnostic_mode_on.htm
tech.root: usbref
ms.assetid: 9b3b7d11-a91c-4905-b639-d9843f05d65e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOCTL_USB_DIAGNOSTIC_MODE_ON, IOCTL_USB_DIAGNOSTIC_MODE_ON control, IOCTL_USB_DIAGNOSTIC_MODE_ON control code [Buses], buses.ioctl_usb_diagnostic_mode_on, usbirp_c1493559-ce0a-4b79-8c7b-5fff2f3c83b3.xml, usbuser/IOCTL_USB_DIAGNOSTIC_MODE_ON
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - usbuser.h
api_name:
 - IOCTL_USB_DIAGNOSTIC_MODE_ON
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_USB_DIAGNOSTIC_MODE_ON IOCTL


## -description



The <b>IOCTL_USB_DIAGNOSTIC_MODE_ON</b> I/O control has been deprecated. Do not use.




## -ioctlparameters




### -input-buffer



<text></text>




### -input-buffer-length



<text></text>




### -output-buffer



<text></text>




### -output-buffer-length



<text></text>




### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block



Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).



