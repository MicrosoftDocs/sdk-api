---
UID: NS:usbuser._USBUSER_BANDWIDTH_INFO_REQUEST
title: "_USBUSER_BANDWIDTH_INFO_REQUEST"
author: windows-sdk-content
description: The USBUSER_BANDWIDTH_INFO_REQUEST structure is used with the IOCTL_USB_USER_REQUEST I/O control request to retrieve information about the allocated bandwidth.
old-location: buses\usbuser_bandwidth_info_request.htm
old-project: usbref
ms.assetid: 146ff4d9-ddd5-42e9-b421-2cac105fe923
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PUSBUSER_BANDWIDTH_INFO_REQUEST, PUSBUSER_BANDWIDTH_INFO_REQUEST, PUSBUSER_BANDWIDTH_INFO_REQUEST structure pointer [Buses], USBUSER_BANDWIDTH_INFO_REQUEST, USBUSER_BANDWIDTH_INFO_REQUEST structure [Buses], _USBUSER_BANDWIDTH_INFO_REQUEST, buses.usbuser_bandwidth_info_request, usbstrct_f688b719-a1cf-4fc1-a2e6-dd391a676703.xml, usbuser/PUSBUSER_BANDWIDTH_INFO_REQUEST, usbuser/USBUSER_BANDWIDTH_INFO_REQUEST"
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
req.typenames: USBUSER_BANDWIDTH_INFO_REQUEST, *PUSBUSER_BANDWIDTH_INFO_REQUEST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - usbuser.h
api_name:
 - USBUSER_BANDWIDTH_INFO_REQUEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _USBUSER_BANDWIDTH_INFO_REQUEST structure


## -description


The <b>USBUSER_BANDWIDTH_INFO_REQUEST</b> structure is used with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve information about the allocated bandwidth.


## -struct-fields




### -field Header

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff539187">USBUSER_REQUEST_HEADER</a> structure that specifies the user-mode request on input to IOCTL_USB_USER_REQUEST and provides buffer and status information on output.


### -field BandwidthInformation

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff539195">USB_BANDWIDTH_INFO</a> structure that reports bandwidth allocation information.


## -remarks



The <b>USBUSER_BANDWIDTH_INFO_REQUEST</b> structure is used with the USBUSER_GET_BANDWIDTH_INFORMATION user-mode request. For more information about this request, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540160">USB Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539187">USBUSER_REQUEST_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539195">USB_BANDWIDTH_INFO</a>
 

 

