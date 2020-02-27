---
UID: NS:usbuser._USBUSER_PASS_THRU_REQUEST
title: USBUSER_PASS_THRU_REQUEST (usbuser.h)
description: The USBUSER_PASS_THRU_REQUEST structure is used in conjunction with the IOCTL_USB_USER_REQUEST I/O control request to send a vendor-specific command to the host controller miniport driver.
old-location: buses\usbuser_pass_thru_request.htm
tech.root: usbref
ms.assetid: 4b04ded7-6641-4390-a5e5-e26603efc757
ms.date: 12/05/2018
ms.keywords: '*PUSBUSER_PASS_THRU_REQUEST, PUSBUSER_PASS_THRU_REQUEST, PUSBUSER_PASS_THRU_REQUEST structure pointer [Buses], USBUSER_PASS_THRU_REQUEST, USBUSER_PASS_THRU_REQUEST structure [Buses], buses.usbuser_pass_thru_request, usbstrct_81650bb7-7b9f-4dc4-af2e-c2a727e7cb4c.xml, usbuser/PUSBUSER_PASS_THRU_REQUEST, usbuser/USBUSER_PASS_THRU_REQUEST'
f1_keywords:
- usbuser/USBUSER_PASS_THRU_REQUEST
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
- USBUSER_PASS_THRU_REQUEST
targetos: Windows
req.typenames: USBUSER_PASS_THRU_REQUEST, *PUSBUSER_PASS_THRU_REQUEST
req.redist: 
ms.custom: 19H1
---

# USBUSER_PASS_THRU_REQUEST structure


## -description


The <b>USBUSER_PASS_THRU_REQUEST</b> structure is used in conjunction with the <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to send a vendor-specific command to the host controller miniport driver.


## -struct-fields




### -field Header

Contains a structure of type <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a> that specifies the user-mode request on input to <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>, and provides buffer and status information on output.


### -field PassThru

Contains a structure of type <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ns-usbuser-usb_pass_thru_parameters">USB_PASS_THRU_PARAMETERS</a> that specifies the parameters associated with this request.


## -remarks



The <b>USBUSER_PASS_THRU_REQUEST</b> structure is used in conjunction with the USBUSER_PASS_THRU user-mode request. For a description of this request, see <a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/index">USB Structures</a>
 

 

