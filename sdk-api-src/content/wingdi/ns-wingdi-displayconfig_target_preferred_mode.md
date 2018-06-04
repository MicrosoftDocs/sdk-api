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

# DISPLAYCONFIG_TARGET_PREFERRED_MODE structure


## -description


The <b>DISPLAYCONFIG_TARGET_PREFERRED_MODE</b> structure contains information about the preferred mode of a display.


## -struct-fields




### -field header

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553920">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains information about the request for the target preferred mode. The caller should set the <b>type</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_PREFERRED_MODE and the <b>adapterId</b> and <b>id</b> members of DISPLAYCONFIG_DEVICE_INFO_HEADER to the target for which the caller wants the preferred mode. The caller should set the <b>size</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to at least the size of the DISPLAYCONFIG_TARGET_PREFERRED_MODE structure.


### -field width

The width in pixels of the best mode for the monitor that is connected to the target that the <b>targetMode</b> member specifies.


### -field height

The height in pixels of the best mode for the monitor that is connected to the target that the <b>targetMode</b> member specifies.


### -field targetMode

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553993">DISPLAYCONFIG_TARGET_MODE</a> structure that describes the best target mode for the monitor that is connected to the specified target.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff553920">DISPLAYCONFIG_DEVICE_INFO_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553993">DISPLAYCONFIG_TARGET_MODE</a>
 

 

