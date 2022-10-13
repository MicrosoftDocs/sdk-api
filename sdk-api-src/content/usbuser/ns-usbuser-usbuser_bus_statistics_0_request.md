---
UID: NS:usbuser._USBUSER_BUS_STATISTICS_0_REQUEST
title: USBUSER_BUS_STATISTICS_0_REQUEST (usbuser.h)
description: The USBUSER_BUS_STATISTICS_0_REQUEST structure is used with the IOCTL_USB_USER_REQUEST I/O control request to retrieve bus statistics.
helpviewer_keywords: ["*PUSBUSER_BUS_STATISTICS_0_REQUEST","PUSBUSER_BUS_STATISTICS_0_REQUEST","PUSBUSER_BUS_STATISTICS_0_REQUEST structure pointer [Buses]","USBUSER_BUS_STATISTICS_0_REQUEST","USBUSER_BUS_STATISTICS_0_REQUEST structure [Buses]","buses.usbuser_bus_statistics_0_request","usbstrct_bf51b053-6add-4de5-95db-95f755f2bc28.xml","usbuser/PUSBUSER_BUS_STATISTICS_0_REQUEST","usbuser/USBUSER_BUS_STATISTICS_0_REQUEST"]
old-location: buses\usbuser_bus_statistics_0_request.htm
tech.root: buses
ms.assetid: 9913bcf7-61ce-4d96-9510-3b8d2117a802
ms.date: 12/05/2018
ms.keywords: '*PUSBUSER_BUS_STATISTICS_0_REQUEST, PUSBUSER_BUS_STATISTICS_0_REQUEST, PUSBUSER_BUS_STATISTICS_0_REQUEST structure pointer [Buses], USBUSER_BUS_STATISTICS_0_REQUEST, USBUSER_BUS_STATISTICS_0_REQUEST structure [Buses], buses.usbuser_bus_statistics_0_request, usbstrct_bf51b053-6add-4de5-95db-95f755f2bc28.xml, usbuser/PUSBUSER_BUS_STATISTICS_0_REQUEST, usbuser/USBUSER_BUS_STATISTICS_0_REQUEST'
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
req.typenames: USBUSER_BUS_STATISTICS_0_REQUEST, *PUSBUSER_BUS_STATISTICS_0_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USBUSER_BUS_STATISTICS_0_REQUEST
 - usbuser/_USBUSER_BUS_STATISTICS_0_REQUEST
 - PUSBUSER_BUS_STATISTICS_0_REQUEST
 - usbuser/PUSBUSER_BUS_STATISTICS_0_REQUEST
 - USBUSER_BUS_STATISTICS_0_REQUEST
 - usbuser/USBUSER_BUS_STATISTICS_0_REQUEST
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
 - USBUSER_BUS_STATISTICS_0_REQUEST
---

# USBUSER_BUS_STATISTICS_0_REQUEST structure


## -description

The <b>USBUSER_BUS_STATISTICS_0_REQUEST</b> structure is used with the <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve bus statistics.

## -struct-fields

### -field Header

A <a href="/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a> structure that specifies the user-mode request on input to IOCTL_USB_USER_REQUEST and provides buffer and status information on output.

### -field BusStatistics0

A <a href="/windows/desktop/api/usbuser/ns-usbuser-usb_bus_statistics_0">USB_BUS_STATISTICS_0</a> structure that reports bus statistics.

## -remarks

The <b>USBUSER_BUS_STATISTICS_0_REQUEST</b> structure is used with the USBUSER_GET_BUS_STATISTICS_0 user-mode request. For more information about this request, see <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.

## -see-also

<a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="/windows-hardware/drivers/usbcon/winusb-functions-for-pipe-policy-modification">USB Structures</a>



<a href="/windows/desktop/api/usbuser/ns-usbuser-usbuser_request_header">USBUSER_REQUEST_HEADER</a>



<a href="/windows/desktop/api/usbuser/ns-usbuser-usb_bus_statistics_0">USB_BUS_STATISTICS_0</a>