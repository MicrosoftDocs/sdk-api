---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _USB_PASS_THRU_PARAMETERS structure


## -description


The <b>USB_PASS_THRU_PARAMETERS</b> structure is used with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a> I/O control request to pass a vendor-specific command to the host controller miniport driver.


## -struct-fields




### -field FunctionGUID

A GUID that identifies the operation for the host controller miniport driver.


### -field ParameterLength

The size, in bytes, of the USB_PASS_THRU_PARAMETERS structure.


### -field Parameters

A variable length array with the parameter data for the command.


## -remarks



The <b>USB_PASS_THRU_PARAMETERS</b> structure is used with the <a href="https://msdn.microsoft.com/4b04ded7-6641-4390-a5e5-e26603efc757">USBUSER_PASS_THRU</a> user-mode request. For more information about this request, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540160">USB Structures</a>
 

 

