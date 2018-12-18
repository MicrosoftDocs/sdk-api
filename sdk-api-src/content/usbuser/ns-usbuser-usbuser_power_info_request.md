---
UID: NS:usbuser._USBUSER_POWER_INFO_REQUEST
title: USBUSER_POWER_INFO_REQUEST
author: windows-sdk-content
description: The USBUSER_POWER_INFO_REQUEST structure is used in conjunction with the IOCTL_USB_USER_REQUEST I/O control request to retrieve power policy information concerning the relationship of a specific system state to the power state of the host controller and the root hub.
old-location: buses\usbuser_power_info_request.htm
tech.root: usbref
ms.assetid: f2d60a3b-0ba9-4c2d-b830-f0eca735434b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PUSBUSER_POWER_INFO_REQUEST, PUSBUSER_POWER_INFO_REQUEST, PUSBUSER_POWER_INFO_REQUEST structure pointer [Buses], USBUSER_POWER_INFO_REQUEST, USBUSER_POWER_INFO_REQUEST structure [Buses], buses.usbuser_power_info_request, usbstrct_1cbb73ef-b3d5-4568-a5b1-ea3a52cbe771.xml, usbuser/PUSBUSER_POWER_INFO_REQUEST, usbuser/USBUSER_POWER_INFO_REQUEST"
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
 - USBUSER_POWER_INFO_REQUEST
product: Windows
targetos: Windows
req.typenames: USBUSER_POWER_INFO_REQUEST, *PUSBUSER_POWER_INFO_REQUEST
req.redist: 
---

# USBUSER_POWER_INFO_REQUEST structure


## -description


The <b>USBUSER_POWER_INFO_REQUEST</b> structure is used in conjunction with the <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve power policy information concerning the relationship of a specific system state to the power state of the host controller and the root hub.


## -struct-fields




### -field Header

Contains a structure of type <a href="https://msdn.microsoft.com/f5f1e136-f603-4f9a-8ebb-8f6ad847e04d">USBUSER_REQUEST_HEADER</a> that specifies the user-mode request on input to <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>, and provides buffer and status information on output.


### -field PowerInformation

Contains a structure of type <a href="https://msdn.microsoft.com/b4f35d7e-b0e3-44d9-8e41-1752cb0af5ef">USB_POWER_INFO</a> that specifies the parameters associated with this request.


## -remarks



The <b>USBUSER_POWER_INFO_REQUEST</b> structure is used in conjunction with the USBUSER_GET_POWER_STATE_MAP user-mode request. For a description of this request, see <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/8ca7033d-6586-4c34-b940-67ddfbe21af9">USB Structures</a>
 

 

