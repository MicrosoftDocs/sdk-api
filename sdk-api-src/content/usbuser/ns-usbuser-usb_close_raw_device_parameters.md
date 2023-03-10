---
UID: NS:usbuser._USB_CLOSE_RAW_DEVICE_PARAMETERS
title: USB_CLOSE_RAW_DEVICE_PARAMETERS (usbuser.h)
description: This structure is not supported. The USB_CLOSE_RAW_DEVICE_PARAMETERS structure is used with the IOCTL_USB_USER_REQUEST I/O control request to close raw access to devices on the bus.
helpviewer_keywords: ["*PUSB_CLOSE_RAW_DEVICE_PARAMETERS","PUSB_CLOSE_RAW_DEVICE_PARAMETERS","PUSB_CLOSE_RAW_DEVICE_PARAMETERS structure pointer [Buses]","USB_CLOSE_RAW_DEVICE_PARAMETERS","USB_CLOSE_RAW_DEVICE_PARAMETERS structure [Buses]","buses.usb_close_raw_device_parameters","usbstrct_aad6430d-1587-4aca-827a-15e391dc0361.xml","usbuser/PUSB_CLOSE_RAW_DEVICE_PARAMETERS","usbuser/USB_CLOSE_RAW_DEVICE_PARAMETERS"]
old-location: buses\usb_close_raw_device_parameters.htm
tech.root: buses
ms.assetid: 00da48bb-4ebe-43b8-85fc-54ce3b183750
ms.date: 12/05/2018
ms.keywords: '*PUSB_CLOSE_RAW_DEVICE_PARAMETERS, PUSB_CLOSE_RAW_DEVICE_PARAMETERS, PUSB_CLOSE_RAW_DEVICE_PARAMETERS structure pointer [Buses], USB_CLOSE_RAW_DEVICE_PARAMETERS, USB_CLOSE_RAW_DEVICE_PARAMETERS structure [Buses], buses.usb_close_raw_device_parameters, usbstrct_aad6430d-1587-4aca-827a-15e391dc0361.xml, usbuser/PUSB_CLOSE_RAW_DEVICE_PARAMETERS, usbuser/USB_CLOSE_RAW_DEVICE_PARAMETERS'
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
req.typenames: USB_CLOSE_RAW_DEVICE_PARAMETERS, *PUSB_CLOSE_RAW_DEVICE_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USB_CLOSE_RAW_DEVICE_PARAMETERS
 - usbuser/_USB_CLOSE_RAW_DEVICE_PARAMETERS
 - PUSB_CLOSE_RAW_DEVICE_PARAMETERS
 - usbuser/PUSB_CLOSE_RAW_DEVICE_PARAMETERS
 - USB_CLOSE_RAW_DEVICE_PARAMETERS
 - usbuser/USB_CLOSE_RAW_DEVICE_PARAMETERS
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
 - USB_CLOSE_RAW_DEVICE_PARAMETERS
---

# USB_CLOSE_RAW_DEVICE_PARAMETERS structure


## -description

This structure is not supported. 

The <b>USB_CLOSE_RAW_DEVICE_PARAMETERS</b> structure is used with the <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to close raw access to devices on the bus.

## -struct-fields

### -field xxx

Reserved.

## -remarks

The USB_CLOSE_RAW_DEVICE_PARAMETERS structure is used with the USBUSER_OP_CLOSE_RAW_DEVICE user-mode request. For a description of this request, see <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.

## -see-also

<a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>