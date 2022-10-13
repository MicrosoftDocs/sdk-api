---
UID: NS:usbuser._USBUSER_BANDWIDTH_INFO_REQUEST
title: USBUSER_BANDWIDTH_INFO_REQUEST (usbuser.h)
description: The USBUSER_BANDWIDTH_INFO_REQUEST structure is used with the IOCTL_USB_USER_REQUEST I/O control request to retrieve information about the allocated bandwidth.
helpviewer_keywords: ["*PUSBUSER_BANDWIDTH_INFO_REQUEST","PUSBUSER_BANDWIDTH_INFO_REQUEST","PUSBUSER_BANDWIDTH_INFO_REQUEST structure pointer [Buses]","USBUSER_BANDWIDTH_INFO_REQUEST","USBUSER_BANDWIDTH_INFO_REQUEST structure [Buses]","buses.usbuser_bandwidth_info_request","usbstrct_f688b719-a1cf-4fc1-a2e6-dd391a676703.xml","usbuser/PUSBUSER_BANDWIDTH_INFO_REQUEST","usbuser/USBUSER_BANDWIDTH_INFO_REQUEST"]
old-location: buses\usbuser_bandwidth_info_request.htm
tech.root: buses
ms.assetid: 146ff4d9-ddd5-42e9-b421-2cac105fe923
ms.date: 12/05/2018
ms.keywords: '*PUSBUSER_BANDWIDTH_INFO_REQUEST, PUSBUSER_BANDWIDTH_INFO_REQUEST, PUSBUSER_BANDWIDTH_INFO_REQUEST structure pointer [Buses], USBUSER_BANDWIDTH_INFO_REQUEST, USBUSER_BANDWIDTH_INFO_REQUEST structure [Buses], buses.usbuser_bandwidth_info_request, usbstrct_f688b719-a1cf-4fc1-a2e6-dd391a676703.xml, usbuser/PUSBUSER_BANDWIDTH_INFO_REQUEST, usbuser/USBUSER_BANDWIDTH_INFO_REQUEST'
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
req.typenames: USBUSER_BANDWIDTH_INFO_REQUEST, *PUSBUSER_BANDWIDTH_INFO_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USBUSER_BANDWIDTH_INFO_REQUEST
 - usbuser/_USBUSER_BANDWIDTH_INFO_REQUEST
 - PUSBUSER_BANDWIDTH_INFO_REQUEST
 - usbuser/PUSBUSER_BANDWIDTH_INFO_REQUEST
 - USBUSER_BANDWIDTH_INFO_REQUEST
 - usbuser/USBUSER_BANDWIDTH_INFO_REQUEST
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
 - USBUSER_BANDWIDTH_INFO_REQUEST
---

# USBUSER_BANDWIDTH_INFO_REQUEST structure


## -description

The <b>USBUSER_BANDWIDTH_INFO_REQUEST</b> structure is used with the <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve information about the allocated bandwidth.

## -struct-fields

### -field Header

A <a href="/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a> structure that specifies the user-mode request on input to IOCTL_USB_USER_REQUEST and provides buffer and status information on output.

### -field BandwidthInformation

A <a href="/windows/desktop/api/usbuser/ns-usbuser-usb_bandwidth_info">USB_BANDWIDTH_INFO</a> structure that reports bandwidth allocation information.

## -remarks

The <b>USBUSER_BANDWIDTH_INFO_REQUEST</b> structure is used with the USBUSER_GET_BANDWIDTH_INFORMATION user-mode request. For more information about this request, see <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.

## -see-also

<a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="/windows-hardware/drivers/usbcon/winusb-functions-for-pipe-policy-modification">USB Structures</a>



<a href="/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a>



<a href="/windows/desktop/api/usbuser/ns-usbuser-usb_bandwidth_info">USB_BANDWIDTH_INFO</a>