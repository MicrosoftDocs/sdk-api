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

# _ELEMENT_TYPE enumeration


## -description


Specifies the element type of a changer device.


## -enum-fields




### -field AllElements

All elements of a changer, including its robotic transport, drives, slots, and insert/eject ports. This value is valid only with 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559396">IOCTL_CHANGER_GET_ELEMENT_STATUS</a> or 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559409">IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS</a>.


### -field ChangerTransport

Robotic transport element, which is used to move media between insert/eject ports, slots, and drives.


### -field ChangerSlot

Storage element, which is a slot in the changer in which media is stored when not mounted in a drive.


### -field ChangerIEPort

Insert/eject port, which is a single- or multiple-cartridge access port in some changers. An element is an insert/eject port only if it is possible to move a piece of media from a slot to the insert/eject port.


### -field ChangerDrive

Data transfer element where data can be read from and written to media.


### -field ChangerDoor

Mechanism that provides access to all media in a changer at one time (as compared to an IEport that provides access to one or more, but not all, media). For example, a large front door or a magazine that contains all media in the changer is an element of this type. This value is valid only with 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559422">IOCTL_CHANGER_SET_ACCESS</a>.


### -field ChangerKeypad

Keypad or other input control on the front panel of a changer. This value is valid only with 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559422">IOCTL_CHANGER_SET_ACCESS</a>.


### -field ChangerMaxElement




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551457">CHANGER_ELEMENT</a>
 

 

