---
UID: NS:usbuser._USB_PASS_THRU_PARAMETERS
title: USB_PASS_THRU_PARAMETERS (usbuser.h)
description: The USB_PASS_THRU_PARAMETERS structure is used with the IOCTL_USB_USER_REQUEST I/O control request to pass a vendor-specific command to the host controller miniport driver.
helpviewer_keywords: ["*PUSB_PASS_THRU_PARAMETERS","PUSB_PASS_THRU_PARAMETERS","PUSB_PASS_THRU_PARAMETERS structure pointer [Buses]","USB_PASS_THRU_PARAMETERS","USB_PASS_THRU_PARAMETERS structure [Buses]","buses.usb_pass_thru_parameters","usbstrct_1e8e5d21-ea79-4617-80c6-4f66f149d16a.xml","usbuser/PUSB_PASS_THRU_PARAMETERS","usbuser/USB_PASS_THRU_PARAMETERS"]
old-location: buses\usb_pass_thru_parameters.htm
tech.root: buses
ms.assetid: 04a29463-af7b-44a4-aac1-20f386c7dd20
ms.date: 12/05/2018
ms.keywords: '*PUSB_PASS_THRU_PARAMETERS, PUSB_PASS_THRU_PARAMETERS, PUSB_PASS_THRU_PARAMETERS structure pointer [Buses], USB_PASS_THRU_PARAMETERS, USB_PASS_THRU_PARAMETERS structure [Buses], buses.usb_pass_thru_parameters, usbstrct_1e8e5d21-ea79-4617-80c6-4f66f149d16a.xml, usbuser/PUSB_PASS_THRU_PARAMETERS, usbuser/USB_PASS_THRU_PARAMETERS'
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
req.typenames: USB_PASS_THRU_PARAMETERS, *PUSB_PASS_THRU_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USB_PASS_THRU_PARAMETERS
 - usbuser/_USB_PASS_THRU_PARAMETERS
 - PUSB_PASS_THRU_PARAMETERS
 - usbuser/PUSB_PASS_THRU_PARAMETERS
 - USB_PASS_THRU_PARAMETERS
 - usbuser/USB_PASS_THRU_PARAMETERS
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
 - USB_PASS_THRU_PARAMETERS
---

# USB_PASS_THRU_PARAMETERS structure


## -description

The <b>USB_PASS_THRU_PARAMETERS</b> structure is used with the <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to pass a vendor-specific command to the host controller miniport driver.

## -struct-fields

### -field FunctionGUID

A GUID that identifies the operation for the host controller miniport driver.

### -field ParameterLength

The size, in bytes, of the USB_PASS_THRU_PARAMETERS structure.

### -field Parameters

A variable length array with the parameter data for the command.

## -remarks

The <b>USB_PASS_THRU_PARAMETERS</b> structure is used with the <a href="/windows/desktop/api/usbuser/ns-usbuser-usbuser_pass_thru_request">USBUSER_PASS_THRU</a> user-mode request. For more information about this request, see <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.

## -see-also

<a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="/windows-hardware/drivers/ddi/content/index">USB Structures</a>