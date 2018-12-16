---
UID: NS:usbuser._USBUSER_CONTROLLER_UNICODE_NAME
title: USBUSER_CONTROLLER_UNICODE_NAME
author: windows-sdk-content
description: The USBUSER_CONTROLLER_UNICODE_NAME structure is used in conjunction with the IOCTL_USB_USER_REQUEST I/O control request to retrieve the USB host controller driverkey name.
old-location: buses\usbuser_controller_unicode_name.htm
tech.root: usbref
ms.assetid: 16c445cb-dac6-49de-b376-cee47644924d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PUSBUSER_CONTROLLER_UNICODE_NAME, PUSBUSER_CONTROLLER_UNICODE_NAME, PUSBUSER_CONTROLLER_UNICODE_NAME structure pointer [Buses], USBUSER_CONTROLLER_UNICODE_NAME, USBUSER_CONTROLLER_UNICODE_NAME structure [Buses], buses.usbuser_controller_unicode_name, usbstrct_c2cd9d6c-f92a-4478-9e4b-bf71ff834888.xml, usbuser/PUSBUSER_CONTROLLER_UNICODE_NAME, usbuser/USBUSER_CONTROLLER_UNICODE_NAME"
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: USBUSER_CONTROLLER_UNICODE_NAME, *PUSBUSER_CONTROLLER_UNICODE_NAME
req.redist: 
---

# USBUSER_CONTROLLER_UNICODE_NAME structure


## -description


The <b>USBUSER_CONTROLLER_UNICODE_NAME</b> structure is used in conjunction with the <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve the USB host controller driverkey name.


## -struct-fields




### -field Header

Contains a structure of type <a href="https://msdn.microsoft.com/f5f1e136-f603-4f9a-8ebb-8f6ad847e04d">USBUSER_REQUEST_HEADER</a> that specifies the user-mode request on input to <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>, and provides buffer and status information on output.


### -field UnicodeName

Contains a Unicode string of type <a href="https://msdn.microsoft.com/d388332c-2f7c-410f-88f4-d0e56fed7a99">USB_UNICODE_NAME</a> that reports the host controller's driverkey name.


## -remarks



The <b>USBUSER_CONTROLLER_UNICODE_NAME</b> structure is used in conjunction with the USBUSER_GET_CONTROLLER_DRIVER_KEY user-mode request. For a description of this request, see <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/8ca7033d-6586-4c34-b940-67ddfbe21af9">USB Structures</a>



<a href="https://msdn.microsoft.com/f5f1e136-f603-4f9a-8ebb-8f6ad847e04d">USBUSER_REQUEST_HEADER</a>



<a href="https://msdn.microsoft.com/d388332c-2f7c-410f-88f4-d0e56fed7a99">USB_UNICODE_NAME</a>
 

 

