---
UID: NS:usbuser._USBUSER_CONTROLLER_UNICODE_NAME
title: "_USBUSER_CONTROLLER_UNICODE_NAME"
author: windows-sdk-content
description: The USBUSER_CONTROLLER_UNICODE_NAME structure is used in conjunction with the IOCTL_USB_USER_REQUEST I/O control request to retrieve the USB host controller driverkey name.
old-location: buses\usbuser_controller_unicode_name.htm
old-project: usbref
ms.assetid: 16c445cb-dac6-49de-b376-cee47644924d
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: "*PUSBUSER_CONTROLLER_UNICODE_NAME, PUSBUSER_CONTROLLER_UNICODE_NAME, PUSBUSER_CONTROLLER_UNICODE_NAME structure pointer [Buses], USBUSER_CONTROLLER_UNICODE_NAME, USBUSER_CONTROLLER_UNICODE_NAME structure [Buses], _USBUSER_CONTROLLER_UNICODE_NAME, buses.usbuser_controller_unicode_name, usbstrct_c2cd9d6c-f92a-4478-9e4b-bf71ff834888.xml, usbuser/PUSBUSER_CONTROLLER_UNICODE_NAME, usbuser/USBUSER_CONTROLLER_UNICODE_NAME"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: USBUSER_CONTROLLER_UNICODE_NAME, *PUSBUSER_CONTROLLER_UNICODE_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	usbuser.h
api_name:
-	USBUSER_CONTROLLER_UNICODE_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _USBUSER_CONTROLLER_UNICODE_NAME structure


## -description


The <b>USBUSER_CONTROLLER_UNICODE_NAME</b> structure is used in conjunction with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve the USB host controller driverkey name.


## -struct-fields




### -field Header

Contains a structure of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff539187">USBUSER_REQUEST_HEADER</a> that specifies the user-mode request on input to <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>, and provides buffer and status information on output.


### -field UnicodeName

Contains a Unicode string of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff540168">USB_UNICODE_NAME</a> that reports the host controller's driverkey name.


## -remarks



The <b>USBUSER_CONTROLLER_UNICODE_NAME</b> structure is used in conjunction with the USBUSER_GET_CONTROLLER_DRIVER_KEY user-mode request. For a description of this request, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540160">USB Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539187">USBUSER_REQUEST_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540168">USB_UNICODE_NAME</a>
 

 

