---
UID: NS:usbuser._USBUSER_GET_DRIVER_VERSION
title: "_USBUSER_GET_DRIVER_VERSION"
author: windows-sdk-content
description: The USBUSER_GET_DRIVER_VERSION structure is used with the IOCTL_USB_USER_REQUEST I/O control request to read driver and interface version information.
old-location: buses\usbuser_get_driver_version.htm
tech.root: usbref
ms.assetid: 415eefbb-e39a-43fa-9fff-49799f74fbd6
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*PUSBUSER_GET_DRIVER_VERSION, PUSBUSER_GET_DRIVER_VERSION, PUSBUSER_GET_DRIVER_VERSION structure pointer [Buses], USBUSER_GET_DRIVER_VERSION, USBUSER_GET_DRIVER_VERSION structure [Buses], _USBUSER_GET_DRIVER_VERSION, buses.usbuser_get_driver_version, usbstrct_adb61812-7474-4eae-bf31-9b2c9a03962f.xml, usbuser/PUSBUSER_GET_DRIVER_VERSION, usbuser/USBUSER_GET_DRIVER_VERSION"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - USBUSER_GET_DRIVER_VERSION
product: Windows
targetos: Windows
req.typenames: USBUSER_GET_DRIVER_VERSION, *PUSBUSER_GET_DRIVER_VERSION
req.redist: 
---

# _USBUSER_GET_DRIVER_VERSION structure


## -description


The <b>USBUSER_GET_DRIVER_VERSION</b> structure is used with the <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a> I/O control request to read driver and interface version information.


## -struct-fields




### -field Header

A <a href="https://msdn.microsoft.com/f5f1e136-f603-4f9a-8ebb-8f6ad847e04d">USBUSER_REQUEST_HEADER</a> structure that specifies the user-mode request on input to <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a> and provides buffer and status information on output.


### -field Parameters

A <a href="https://msdn.microsoft.com/0d90e857-c3bb-484d-8895-1a29fdf656b1">USB_DRIVER_VERSION_PARAMETERS</a> structure that specifies the parameters that are associated with this request.


## -remarks



The <b>USBUSER_GET_DRIVER_VERSION</b> structure is used with the USBUSER_GET_USB_DRIVER_VERSION user-mode request. For more information about this request, see <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/8ca7033d-6586-4c34-b940-67ddfbe21af9">USB Structures</a>



<a href="https://msdn.microsoft.com/f5f1e136-f603-4f9a-8ebb-8f6ad847e04d">USBUSER_REQUEST_HEADER</a>



<a href="https://msdn.microsoft.com/0d90e857-c3bb-484d-8895-1a29fdf656b1">USB_DRIVER_VERSION_PARAMETERS</a>
 

 

