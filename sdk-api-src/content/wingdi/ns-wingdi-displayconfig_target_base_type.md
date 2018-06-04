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

# DISPLAYCONFIG_TARGET_BASE_TYPE structure


## -description


Specifies base output technology info for a given target ID.


## -struct-fields




### -field header

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553920">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains info about the request for the target device name. The caller should set the <b>type</b> member of <b>DISPLAYCONFIG_DEVICE_INFO_HEADER</b> to <b>DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_BASE_TYPE</b> and the <b>adapterId</b> and <b>id</b> members of <b>DISPLAYCONFIG_DEVICE_INFO_HEADER</b> to the target for which the caller wants the target device name.

 The caller should set the <b>size</b> member of <a href="https://msdn.microsoft.com/library/windows/hardware/ff553920">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> to at least the size of the <b>DISPLAYCONFIG_TARGET_BASE_TYPE</b> structure.


### -field baseOutputTechnology

The base output technology, given as a constant value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff554003">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a> enumeration, of the adapter and the target specified by the <b>header</b> member. See Remarks.


## -remarks



For a Miracast display device, a call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553903">DisplayConfigGetDeviceInfo</a>  function always returns  a value of <a href="https://msdn.microsoft.com/library/windows/hardware/ff554003">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a>.<b>DISPLAYCONFIG_OUTPUT_TECHNOLOGY_MIRACAST</b>, regardless of what the Miracast sink reports as the connector type.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff553920">DISPLAYCONFIG_DEVICE_INFO_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554003">DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553903">DisplayConfigGetDeviceInfo</a>
 

 

