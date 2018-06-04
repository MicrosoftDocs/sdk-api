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

# DISPLAYCONFIG_PATH_INFO structure


## -description


The DISPLAYCONFIG_PATH_INFO structure is used to describe a single path from a target to a source.


## -struct-fields




### -field sourceInfo

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553951">DISPLAYCONFIG_PATH_SOURCE_INFO</a> structure that contains the source information for the path.


### -field targetInfo

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553954">DISPLAYCONFIG_PATH_TARGET_INFO</a> structure that contains the target information for the path.


### -field flags

A bitwise OR of flag values that indicates the state of the path. The following values are supported:





#### DISPLAYCONFIG_PATH_ACTIVE

Set by <a href="https://msdn.microsoft.com/library/windows/hardware/ff569215">QueryDisplayConfig</a> to indicate that the path is active and part of the desktop. If this flag value is set, <a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a> attempts to enable this path.



#### DISPLAYCONFIG_PATH_SUPPORT_VIRTUAL_MODE

Set by <a href="https://msdn.microsoft.com/library/windows/hardware/ff569215">QueryDisplayConfig</a> to indicate that the path supports the virtual mode. Supported starting in Windows 10.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff553951">DISPLAYCONFIG_PATH_SOURCE_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553954">DISPLAYCONFIG_PATH_TARGET_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569215">QueryDisplayConfig</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a>
 

 

