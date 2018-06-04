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

# _WINUSB_SETUP_PACKET structure


## -description


The <b>WINUSB_SETUP_PACKE</b>T structure describes a USB setup packet.


## -struct-fields




### -field RequestType

The request type. The values that are assigned to this member are defined in Table 9.2 of section 9.3 of the Universal Serial Bus (USB) specification (www.usb.org). 


### -field Request

The device request. The values that are assigned to this member are defined in Table 9.3 of section 9.4 of the Universal Serial Bus (USB) specification.


### -field Value

The meaning of this member varies according to the request. For an explanation of this member, see the Universal Serial Bus (USB) specification.


### -field Index

The meaning of this member varies according to the request. For an explanation of this member, see the Universal Serial Bus (USB) specification.


### -field Length

The number of bytes to transfer.


## -remarks



Callers of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540219">WinUsb_ControlTransfer</a> routine must pass in a <b>WINUSB_SETUP_PACKET</b> structure. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540160">USB Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540219">WinUsb_ControlTransfer</a>
 

 

