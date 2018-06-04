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

# DISPLAYCONFIG_MODE_INFO_TYPE enumeration


## -description


The DISPLAYCONFIG_MODE_INFO_TYPE enumeration specifies that the information that is contained within the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553933">DISPLAYCONFIG_MODE_INFO</a> structure is either source or target mode.


## -enum-fields




### -field DISPLAYCONFIG_MODE_INFO_TYPE_SOURCE

Indicates that the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553933">DISPLAYCONFIG_MODE_INFO</a> structure contains source mode information.


### -field DISPLAYCONFIG_MODE_INFO_TYPE_TARGET

Indicates that the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553933">DISPLAYCONFIG_MODE_INFO</a> structure contains target mode information.


### -field DISPLAYCONFIG_MODE_INFO_TYPE_DESKTOP_IMAGE

Indicates that the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553933">DISPLAYCONFIG_MODE_INFO</a> structure contains a valid <a href="https://msdn.microsoft.com/library/windows/hardware/mt622102">DISPLAYCONFIG_DESKTOP_IMAGE_INFO</a> structure. Supported starting in Windows 10.


### -field DISPLAYCONFIG_MODE_INFO_TYPE_FORCE_UINT32

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff553933">DISPLAYCONFIG_MODE_INFO</a>
 

 

