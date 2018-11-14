---
UID: NS:usbuser._USBUSER_BUS_STATISTICS_0_REQUEST
title: "_USBUSER_BUS_STATISTICS_0_REQUEST"
author: windows-sdk-content
description: The USBUSER_BUS_STATISTICS_0_REQUEST structure is used with the IOCTL_USB_USER_REQUEST I/O control request to retrieve bus statistics.
old-location: buses\usbuser_bus_statistics_0_request.htm
tech.root: usbref
ms.assetid: 9913bcf7-61ce-4d96-9510-3b8d2117a802
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: "*PUSBUSER_BUS_STATISTICS_0_REQUEST, PUSBUSER_BUS_STATISTICS_0_REQUEST, PUSBUSER_BUS_STATISTICS_0_REQUEST structure pointer [Buses], USBUSER_BUS_STATISTICS_0_REQUEST, USBUSER_BUS_STATISTICS_0_REQUEST structure [Buses], _USBUSER_BUS_STATISTICS_0_REQUEST, buses.usbuser_bus_statistics_0_request, usbstrct_bf51b053-6add-4de5-95db-95f755f2bc28.xml, usbuser/PUSBUSER_BUS_STATISTICS_0_REQUEST, usbuser/USBUSER_BUS_STATISTICS_0_REQUEST"
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
 - USBUSER_BUS_STATISTICS_0_REQUEST
product: Windows
targetos: Windows
req.typenames: USBUSER_BUS_STATISTICS_0_REQUEST, *PUSBUSER_BUS_STATISTICS_0_REQUEST
req.redist: 
---

# _USBUSER_BUS_STATISTICS_0_REQUEST structure


## -description


The <b>USBUSER_BUS_STATISTICS_0_REQUEST</b> structure is used with the <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve bus statistics.


## -struct-fields




### -field Header

A <a href="https://msdn.microsoft.com/f5f1e136-f603-4f9a-8ebb-8f6ad847e04d">USBUSER_REQUEST_HEADER</a> structure that specifies the user-mode request on input to IOCTL_USB_USER_REQUEST and provides buffer and status information on output.


### -field BusStatistics0

A <a href="https://msdn.microsoft.com/d9673718-c39c-4f26-8d59-553366b8bd0a">USB_BUS_STATISTICS_0</a> structure that reports bus statistics.


## -remarks



The <b>USBUSER_BUS_STATISTICS_0_REQUEST</b> structure is used with the USBUSER_GET_BUS_STATISTICS_0 user-mode request. For more information about this request, see <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/8ca7033d-6586-4c34-b940-67ddfbe21af9">USB Structures</a>



<a href="https://msdn.microsoft.com/f5f1e136-f603-4f9a-8ebb-8f6ad847e04d">USBUSER_REQUEST_HEADER</a>



<a href="https://msdn.microsoft.com/d9673718-c39c-4f26-8d59-553366b8bd0a">USB_BUS_STATISTICS_0</a>
 

 

