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

# _MOUSE_UNIT_ID_PARAMETER structure


## -description


MOUSE_UNIT_ID_PARAMETER specifies a unit ID that Mouclass assigns to a mouse.


## -struct-fields




### -field UnitId

Specifies the unit number of the mouse device. A mouse <a href="https://msdn.microsoft.com/dfcc7338-7c4d-4b4c-9a13-c76bfe82f5a9">device name</a> has the format \Device\PointerPort<i>N</i>, where the suffix <i>N </i>is the unit number of the device. For example, a device, whose name is \Device\PointerPort0, has a unit number of zero, and a device, whose name is \Device\PointerPort1, has a unit number of one.


## -remarks



Although this structure is used with an <a href="https://msdn.microsoft.com/library/windows/hardware/ff542080">IOCTL_MOUSE_QUERY_ATTRIBUTES</a> request, Mouclass does not use the <b>UnitId</b> value.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff542080">IOCTL_MOUSE_QUERY_ATTRIBUTES</a>
 

 

