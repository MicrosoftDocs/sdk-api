---
UID: NS:usbuser._USB_PASS_THRU_PARAMETERS
title: "_USB_PASS_THRU_PARAMETERS"
author: windows-sdk-content
description: The USB_PASS_THRU_PARAMETERS structure is used with the IOCTL_USB_USER_REQUEST I/O control request to pass a vendor-specific command to the host controller miniport driver.
old-location: buses\usb_pass_thru_parameters.htm
tech.root: usbref
ms.assetid: 04a29463-af7b-44a4-aac1-20f386c7dd20
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*PUSB_PASS_THRU_PARAMETERS, PUSB_PASS_THRU_PARAMETERS, PUSB_PASS_THRU_PARAMETERS structure pointer [Buses], USB_PASS_THRU_PARAMETERS, USB_PASS_THRU_PARAMETERS structure [Buses], _USB_PASS_THRU_PARAMETERS, buses.usb_pass_thru_parameters, usbstrct_1e8e5d21-ea79-4617-80c6-4f66f149d16a.xml, usbuser/PUSB_PASS_THRU_PARAMETERS, usbuser/USB_PASS_THRU_PARAMETERS"
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
 - USB_PASS_THRU_PARAMETERS
product: Windows
targetos: Windows
req.typenames: USB_PASS_THRU_PARAMETERS, *PUSB_PASS_THRU_PARAMETERS
req.redist: 
---

# _USB_PASS_THRU_PARAMETERS structure


## -description


The <b>USB_PASS_THRU_PARAMETERS</b> structure is used with the <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a> I/O control request to pass a vendor-specific command to the host controller miniport driver.


## -struct-fields




### -field FunctionGUID

A GUID that identifies the operation for the host controller miniport driver.


### -field ParameterLength

The size, in bytes, of the USB_PASS_THRU_PARAMETERS structure.


### -field Parameters

A variable length array with the parameter data for the command.


## -remarks



The <b>USB_PASS_THRU_PARAMETERS</b> structure is used with the <a href="https://msdn.microsoft.com/4b04ded7-6641-4390-a5e5-e26603efc757">USBUSER_PASS_THRU</a> user-mode request. For more information about this request, see <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/8ca7033d-6586-4c34-b940-67ddfbe21af9">USB Structures</a>
 

 

