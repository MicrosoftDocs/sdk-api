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

# DISPLAYCONFIG_DEVICE_INFO_HEADER structure


## -description


The DISPLAYCONFIG_DEVICE_INFO_HEADER structure contains display information about the device.


## -struct-fields




### -field type

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553924">DISPLAYCONFIG_DEVICE_INFO_TYPE</a> enumerated value that determines the type of device information to retrieve or set. The remainder of the packet for the retrieve or set operation follows immediately after the DISPLAYCONFIG_DEVICE_INFO_HEADER structure. 


### -field size

The size, in bytes, of the device information that is retrieved or set. This size includes the size of the header and the size of the additional data that follows the header. This device information depends on the request type. 


### -field adapterId

A locally unique identifier (LUID) that identifies the adapter that the device information packet refers to.


### -field id

The source or target identifier to get or set the device information for. The meaning of this identifier is related to the type of information being requested. For example, in the case of DISPLAYCONFIG_DEVICE_INFO_GET_SOURCE_NAME, this is the source identifier. 


## -remarks



The <a href="https://msdn.microsoft.com/library/windows/hardware/ff553903">DisplayConfigGetDeviceInfo</a> function uses the DISPLAYCONFIG_DEVICE_INFO_HEADER structure for retrieving display configuration information about the device, and the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553909">DisplayConfigSetDeviceInfo</a> function uses the DISPLAYCONFIG_DEVICE_INFO_HEADER structure for setting display configuration information for the device.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff553924">DISPLAYCONFIG_DEVICE_INFO_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553903">DisplayConfigGetDeviceInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553909">DisplayConfigSetDeviceInfo</a>
 

 

