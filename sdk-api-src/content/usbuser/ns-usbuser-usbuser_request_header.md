---
UID: NS:usbuser._USBUSER_REQUEST_HEADER
title: USBUSER_REQUEST_HEADER (usbuser.h)
description: The USBUSER_REQUEST_HEADER structure is used with the IOCTL_USB_USER_REQUEST I/O control request to send a user-mode request to the USB host controller driver.
helpviewer_keywords: ["*PUSBUSER_REQUEST_HEADER","PUSBUSER_REQUEST_HEADER","PUSBUSER_REQUEST_HEADER structure pointer [Buses]","USBUSER_REQUEST_HEADER","USBUSER_REQUEST_HEADER structure [Buses]","buses.usbuser_request_header","usbstrct_04ac2f33-ce32-4697-89d0-5f2c1516c3b6.xml","usbuser/PUSBUSER_REQUEST_HEADER","usbuser/USBUSER_REQUEST_HEADER"]
old-location: buses\usbuser_request_header.htm
tech.root: buses
ms.assetid: f5f1e136-f603-4f9a-8ebb-8f6ad847e04d
ms.date: 12/05/2018
ms.keywords: '*PUSBUSER_REQUEST_HEADER, PUSBUSER_REQUEST_HEADER, PUSBUSER_REQUEST_HEADER structure pointer [Buses], USBUSER_REQUEST_HEADER, USBUSER_REQUEST_HEADER structure [Buses], buses.usbuser_request_header, usbstrct_04ac2f33-ce32-4697-89d0-5f2c1516c3b6.xml, usbuser/PUSBUSER_REQUEST_HEADER, usbuser/USBUSER_REQUEST_HEADER'
req.header: usbuser.h
req.include-header: Usbuser.h
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
req.typenames: USBUSER_REQUEST_HEADER, *PUSBUSER_REQUEST_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USBUSER_REQUEST_HEADER
 - usbuser/_USBUSER_REQUEST_HEADER
 - PUSBUSER_REQUEST_HEADER
 - usbuser/PUSBUSER_REQUEST_HEADER
 - USBUSER_REQUEST_HEADER
 - usbuser/USBUSER_REQUEST_HEADER
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
 - USBUSER_REQUEST_HEADER
---

# USBUSER_REQUEST_HEADER structure


## -description

The <b>USBUSER_REQUEST_HEADER</b> structure is used with the <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to send a user-mode request to the USB host controller driver.

## -struct-fields

### -field UsbUserRequest

The user-mode request. For a list and description of possible values for this member, see <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.

### -field UsbUserStatusCode

The status code that is returned by port driver.

### -field RequestBufferLength

The size, in bytes, of the data buffer. The same buffer is used for both input and output.

### -field ActualBufferLength

The size, in bytes, of the data that is retrieved by the request.

## -remarks

The <b>USBUSER_REQUEST_HEADER</b> structure is used with the <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to send a user-mode request to the USB port driver.

## -see-also

<a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="/windows-hardware/drivers/ddi/content/index">USB Structures</a>