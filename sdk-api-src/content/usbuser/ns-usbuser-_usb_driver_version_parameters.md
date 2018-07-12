---
UID: NS:usbuser._USB_DRIVER_VERSION_PARAMETERS
title: "_USB_DRIVER_VERSION_PARAMETERS"
author: windows-sdk-content
description: The USB_DRIVER_VERSION_PARAMETERS structure is used with the IOCTL_USB_USER_REQUEST I/O control request to retrieve version information.
old-location: buses\usb_driver_version_parameters.htm
old-project: usbref
ms.assetid: 0d90e857-c3bb-484d-8895-1a29fdf656b1
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: "*PUSB_DRIVER_VERSION_PARAMETERS, PUSB_DRIVER_VERSION_PARAMETERS, PUSB_DRIVER_VERSION_PARAMETERS structure pointer [Buses], USB_DRIVER_VERSION_PARAMETERS, USB_DRIVER_VERSION_PARAMETERS structure [Buses], _USB_DRIVER_VERSION_PARAMETERS, buses.usb_driver_version_parameters, usbstrct_267b4211-9852-45ca-afde-9aa35274af90.xml, usbuser/PUSB_DRIVER_VERSION_PARAMETERS, usbuser/USB_DRIVER_VERSION_PARAMETERS"
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
tech.root: 
req.typenames: USB_DRIVER_VERSION_PARAMETERS, *PUSB_DRIVER_VERSION_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - usbuser.h
api_name:
 - USB_DRIVER_VERSION_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _USB_DRIVER_VERSION_PARAMETERS structure


## -description


The <b>USB_DRIVER_VERSION_PARAMETERS</b> structure is used with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve version information.


## -struct-fields




### -field DriverTrackingCode

A tracking code that identifies the revision of the USB stack.


### -field USBDI_Version

The version of the USB driver interface that the USB stack supports.


### -field USBUSER_Version

The version of the USB user interface that the USB stack supports.


### -field CheckedPortDriver

A Boolean value that indicates whether the checked version of the host controller driver is loaded. If <b>TRUE</b>, the checked version of the host controller driver is loaded. If <b>FALSE</b>, the checked version is not loaded.


### -field CheckedMiniportDriver

A Boolean value that indicates whether the checked version of the host controller miniport driver is loaded. If <b>TRUE</b>, the checked version of the host controller miniport driver is loaded. If <b>FALSE</b>, the checked version is not loaded.


### -field USB_Version

The USB version that the USB stack supports. A value of 0x0110 indicates that the USB stack supports version 1.1. A value of 0x0200 indicates the USB stack supports version 2.0.


## -remarks



The <b>USB_DRIVER_VERSION_PARAMETERS</b> structure is used with the USBUSER_GET_USB_DRIVER_VERSION user-mode request. For a description of this request, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540160">USB Structures</a>
 

 

