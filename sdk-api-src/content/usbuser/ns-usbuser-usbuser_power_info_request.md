---
UID: NS:usbuser._USBUSER_POWER_INFO_REQUEST
title: USBUSER_POWER_INFO_REQUEST (usbuser.h)
description: The USBUSER_POWER_INFO_REQUEST structure is used in conjunction with the IOCTL_USB_USER_REQUEST I/O control request to retrieve power policy information concerning the relationship of a specific system state to the power state of the host controller and the root hub.
helpviewer_keywords: ["*PUSBUSER_POWER_INFO_REQUEST","PUSBUSER_POWER_INFO_REQUEST","PUSBUSER_POWER_INFO_REQUEST structure pointer [Buses]","USBUSER_POWER_INFO_REQUEST","USBUSER_POWER_INFO_REQUEST structure [Buses]","buses.usbuser_power_info_request","usbstrct_1cbb73ef-b3d5-4568-a5b1-ea3a52cbe771.xml","usbuser/PUSBUSER_POWER_INFO_REQUEST","usbuser/USBUSER_POWER_INFO_REQUEST"]
old-location: buses\usbuser_power_info_request.htm
tech.root: buses
ms.assetid: f2d60a3b-0ba9-4c2d-b830-f0eca735434b
ms.date: 12/05/2018
ms.keywords: '*PUSBUSER_POWER_INFO_REQUEST, PUSBUSER_POWER_INFO_REQUEST, PUSBUSER_POWER_INFO_REQUEST structure pointer [Buses], USBUSER_POWER_INFO_REQUEST, USBUSER_POWER_INFO_REQUEST structure [Buses], buses.usbuser_power_info_request, usbstrct_1cbb73ef-b3d5-4568-a5b1-ea3a52cbe771.xml, usbuser/PUSBUSER_POWER_INFO_REQUEST, usbuser/USBUSER_POWER_INFO_REQUEST'
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
req.typenames: USBUSER_POWER_INFO_REQUEST, *PUSBUSER_POWER_INFO_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USBUSER_POWER_INFO_REQUEST
 - usbuser/_USBUSER_POWER_INFO_REQUEST
 - PUSBUSER_POWER_INFO_REQUEST
 - usbuser/PUSBUSER_POWER_INFO_REQUEST
 - USBUSER_POWER_INFO_REQUEST
 - usbuser/USBUSER_POWER_INFO_REQUEST
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
 - USBUSER_POWER_INFO_REQUEST
---

# USBUSER_POWER_INFO_REQUEST structure


## -description

The <b>USBUSER_POWER_INFO_REQUEST</b> structure is used in conjunction with the <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve power policy information concerning the relationship of a specific system state to the power state of the host controller and the root hub.

## -struct-fields

### -field Header

Contains a structure of type <a href="/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a> that specifies the user-mode request on input to <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>, and provides buffer and status information on output.

### -field PowerInformation

Contains a structure of type <a href="/windows/desktop/api/usbuser/ns-usbuser-usb_power_info">USB_POWER_INFO</a> that specifies the parameters associated with this request.

## -remarks

The <b>USBUSER_POWER_INFO_REQUEST</b> structure is used in conjunction with the USBUSER_GET_POWER_STATE_MAP user-mode request. For a description of this request, see <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.

## -see-also

<a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="/windows-hardware/drivers/ddi/content/index">USB Structures</a>