---
UID: NS:usbuser._USBUSER_GET_DRIVER_VERSION
title: USBUSER_GET_DRIVER_VERSION (usbuser.h)
author: windows-sdk-content
description: The USBUSER_GET_DRIVER_VERSION structure is used with the IOCTL_USB_USER_REQUEST I/O control request to read driver and interface version information.
old-location: buses\usbuser_get_driver_version.htm
tech.root: usbref
ms.assetid: 415eefbb-e39a-43fa-9fff-49799f74fbd6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PUSBUSER_GET_DRIVER_VERSION, PUSBUSER_GET_DRIVER_VERSION, PUSBUSER_GET_DRIVER_VERSION structure pointer [Buses], USBUSER_GET_DRIVER_VERSION, USBUSER_GET_DRIVER_VERSION structure [Buses], buses.usbuser_get_driver_version, usbstrct_adb61812-7474-4eae-bf31-9b2c9a03962f.xml, usbuser/PUSBUSER_GET_DRIVER_VERSION, usbuser/USBUSER_GET_DRIVER_VERSION"
ms.topic: struct
f1_keywords: 
 - "usbuser/USBUSER_GET_DRIVER_VERSION"
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
 - USBUSER_GET_DRIVER_VERSION
product: Windows
targetos: Windows
req.typenames: USBUSER_GET_DRIVER_VERSION, *PUSBUSER_GET_DRIVER_VERSION
req.redist: 
ms.custom: 19H1
---

# USBUSER_GET_DRIVER_VERSION structure


## -description


The <b>USBUSER_GET_DRIVER_VERSION</b> structure is used with the <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to read driver and interface version information.


## -struct-fields




### -field Header

A <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ns-usbuser-_usbuser_request_header">USBUSER_REQUEST_HEADER</a> structure that specifies the user-mode request on input to <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> and provides buffer and status information on output.


### -field Parameters

A <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ns-usbuser-_usb_driver_version_parameters">USB_DRIVER_VERSION_PARAMETERS</a> structure that specifies the parameters that are associated with this request.


## -remarks



The <b>USBUSER_GET_DRIVER_VERSION</b> structure is used with the USBUSER_GET_USB_DRIVER_VERSION user-mode request. For more information about this request, see <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/index">USB Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ns-usbuser-_usbuser_request_header">USBUSER_REQUEST_HEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ns-usbuser-_usb_driver_version_parameters">USB_DRIVER_VERSION_PARAMETERS</a>
 

 

