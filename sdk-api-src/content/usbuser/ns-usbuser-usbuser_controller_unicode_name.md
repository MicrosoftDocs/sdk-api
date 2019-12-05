---
UID: NS:usbuser._USBUSER_CONTROLLER_UNICODE_NAME
title: USBUSER_CONTROLLER_UNICODE_NAME (usbuser.h)
description: The USBUSER_CONTROLLER_UNICODE_NAME structure is used in conjunction with the IOCTL_USB_USER_REQUEST I/O control request to retrieve the USB host controller driverkey name.
old-location: buses\usbuser_controller_unicode_name.htm
tech.root: usbref
ms.assetid: 16c445cb-dac6-49de-b376-cee47644924d
ms.date: 12/05/2018
ms.keywords: '*PUSBUSER_CONTROLLER_UNICODE_NAME, PUSBUSER_CONTROLLER_UNICODE_NAME, PUSBUSER_CONTROLLER_UNICODE_NAME structure pointer [Buses], USBUSER_CONTROLLER_UNICODE_NAME, USBUSER_CONTROLLER_UNICODE_NAME structure [Buses], buses.usbuser_controller_unicode_name, usbstrct_c2cd9d6c-f92a-4478-9e4b-bf71ff834888.xml, usbuser/PUSBUSER_CONTROLLER_UNICODE_NAME, usbuser/USBUSER_CONTROLLER_UNICODE_NAME'
ms.topic: struct
f1_keywords:
- usbuser/USBUSER_CONTROLLER_UNICODE_NAME
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- usbuser.h
api_name:
- USBUSER_CONTROLLER_UNICODE_NAME
targetos: Windows
req.typenames: USBUSER_CONTROLLER_UNICODE_NAME, *PUSBUSER_CONTROLLER_UNICODE_NAME
req.redist: 
ms.custom: 19H1
---

# USBUSER_CONTROLLER_UNICODE_NAME structure


## -description


The <b>USBUSER_CONTROLLER_UNICODE_NAME</b> structure is used in conjunction with the <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve the USB host controller driverkey name.


## -struct-fields




### -field Header

Contains a structure of type <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a> that specifies the user-mode request on input to <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>, and provides buffer and status information on output.


### -field UnicodeName

Contains a Unicode string of type <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ns-usbuser-usb_unicode_name">USB_UNICODE_NAME</a> that reports the host controller's driverkey name.


## -remarks



The <b>USBUSER_CONTROLLER_UNICODE_NAME</b> structure is used in conjunction with the USBUSER_GET_CONTROLLER_DRIVER_KEY user-mode request. For a description of this request, see <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/index">USB Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ns-usbuser-usb_unicode_name">USB_UNICODE_NAME</a>
 

 

