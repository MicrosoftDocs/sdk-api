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

# DISPLAYCONFIG_MODE_INFO structure


## -description


The DISPLAYCONFIG_MODE_INFO structure contains either source mode or target mode information.


## -struct-fields




### -field infoType

A value that indicates whether the <b>DISPLAYCONFIG_MODE_INFO</b> structure represents source or target mode information. If <b>infoType</b> is DISPLAYCONFIG_MODE_INFO_TYPE_TARGET, the <i>targetMode</i> parameter value contains a valid DISPLAYCONFIG_TARGET_MODE structure describing the specified target. If <b>infoType</b> is DISPLAYCONFIG_MODE_INFO_TYPE_SOURCE, the <i>sourceMode</i> parameter value contains a valid DISPLAYCONFIG_SOURCE_MODE structure describing the specified source. 


### -field id

The source or target identifier on the specified adapter that this path relates to.


### -field adapterId

The identifier of the adapter that this source or target mode information relates to.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.targetMode

A valid <a href="https://msdn.microsoft.com/library/windows/hardware/ff553993">DISPLAYCONFIG_TARGET_MODE</a> structure that describes the specified target only when <b>infoType</b> is DISPLAYCONFIG_MODE_INFO_TYPE_TARGET.


### -field DUMMYUNIONNAME.sourceMode

A valid <a href="https://msdn.microsoft.com/library/windows/hardware/ff553986">DISPLAYCONFIG_SOURCE_MODE</a> structure that describes the specified source only when <b>infoType</b> is DISPLAYCONFIG_MODE_INFO_TYPE_SOURCE.


### -field DUMMYUNIONNAME.desktopImageInfo

A <a href="https://msdn.microsoft.com/library/windows/hardware/mt622102">DISPLAYCONFIG_DESKTOP_IMAGE_INFO</a> structure that describes information about the desktop image only when <b>infoType</b> is DISPLAYCONFIG_MODE_INFO_TYPE_. 

Supported starting in Windows 10.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff553942">DISPLAYCONFIG_MODE_INFO_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553986">DISPLAYCONFIG_SOURCE_MODE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553993">DISPLAYCONFIG_TARGET_MODE</a>
 

 

