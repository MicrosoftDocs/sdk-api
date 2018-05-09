---
UID: NS:usbuser._USBUSER_PASS_THRU_REQUEST
title: "_USBUSER_PASS_THRU_REQUEST"
author: windows-driver-content
description: The USBUSER_PASS_THRU_REQUEST structure is used in conjunction with the IOCTL_USB_USER_REQUEST I/O control request to send a vendor-specific command to the host controller miniport driver.
old-location: buses\usbuser_pass_thru_request.htm
old-project: usbref
ms.assetid: 4b04ded7-6641-4390-a5e5-e26603efc757
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PUSBUSER_PASS_THRU_REQUEST, PUSBUSER_PASS_THRU_REQUEST, PUSBUSER_PASS_THRU_REQUEST structure pointer [Buses], USBUSER_PASS_THRU_REQUEST, USBUSER_PASS_THRU_REQUEST structure [Buses], _USBUSER_PASS_THRU_REQUEST, buses.usbuser_pass_thru_request, usbstrct_81650bb7-7b9f-4dc4-af2e-c2a727e7cb4c.xml, usbuser/PUSBUSER_PASS_THRU_REQUEST, usbuser/USBUSER_PASS_THRU_REQUEST"
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
req.typenames: USBUSER_PASS_THRU_REQUEST, *PUSBUSER_PASS_THRU_REQUEST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	usbuser.h
api_name:
-	USBUSER_PASS_THRU_REQUEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _USBUSER_PASS_THRU_REQUEST structure


## -description


The <b>USBUSER_PASS_THRU_REQUEST</b> structure is used in conjunction with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a> I/O control request to send a vendor-specific command to the host controller miniport driver.


## -struct-fields




### -field Header

Contains a structure of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff539187">USBUSER_REQUEST_HEADER</a> that specifies the user-mode request on input to <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>, and provides buffer and status information on output.


### -field PassThru

Contains a structure of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff540114">USB_PASS_THRU_PARAMETERS</a> that specifies the parameters associated with this request.


## -remarks



The <b>USBUSER_PASS_THRU_REQUEST</b> structure is used in conjunction with the USBUSER_PASS_THRU user-mode request. For a description of this request, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540160">USB Structures</a>
 

 

