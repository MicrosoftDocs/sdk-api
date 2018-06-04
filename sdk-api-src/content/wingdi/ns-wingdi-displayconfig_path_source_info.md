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

# DISPLAYCONFIG_PATH_SOURCE_INFO structure


## -description


The DISPLAYCONFIG_PATH_SOURCE_INFO structure contains source information for a single path.


## -struct-fields




### -field adapterId

The identifier of the adapter that this source information relates to. 


### -field id

The source identifier on the specified adapter that this path relates to. 


### -field DUMMYUNIONNAME


### -field DUMMYUNIONNAME.modeInfoIdx

A valid index into the mode information table that contains the source mode information for this path only when DISPLAYCONFIG_PATH_SUPPORT_VIRTUAL_MODE is not set. If source mode information is not available, the value of <b>modeInfoIdx</b> is DISPLAYCONFIG_PATH_MODE_IDX_INVALID.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.cloneGroupId

A valid identifier used to show which clone group the path is a member of only when DISPLAYCONFIG_PATH_SUPPORT_VIRTUAL_MODE is set. If this value is invalid, then it must be set to DISPLAYCONFIG_PATH_CLONE_GROUP_INVALID.

<b>cloneGroupId</b> is only used when the source mode index is not specified. Two such scenarios are when the source mode info must be invalid because SDC_TOPOLOGY_SUPPLIED is used, and when SDC_USE_SUPPLIED_DISPLAY_CONFIG is used with paths that do not have source mode info.  The <b>cloneGroupId</b> will be used to indicate which paths are in a clone group, all the paths with the same <b>cloneGroupId</b> value are considered in the same clone group.  There is no requirement that the clone group id’s have to be zero based or contiguous. Supported starting in Windows 10. 



### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.sourceModeInfoIdx

A valid index into the mode array of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553986">DISPLAYCONFIG_SOURCE_MODE</a> entry that contains the source mode information for this path only when DISPLAYCONFIG_PATH_SUPPORT_VIRTUAL_MODE is set. If there is no entry for this in the mode array, the value of <b>sourceModeInfoIdx</b> is DISPLAYCONFIG_PATH_SOURCE_MODE_IDX_INVALID. Supported starting in Windows 10.


### -field statusFlags

A bitwise OR of flag values that indicates the status of the source. The following values are supported:





#### DISPLAYCONFIG_SOURCE_IN_USE

This source is in use by at least one active path.


## -remarks



A DISPLAYCONFIG_PATH_SOURCE_INFO structure is specified in the <b>sourceInfo</b> member of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff553945">DISPLAYCONFIG_PATH_INFO</a> structure.

A source corresponds to a surface on which the display adapter can render pixels. Each display adapter is capable of rendering to x number of sources. What this means is how many desktops can be rendered for extend mode. This is typically 2. For example, source 0 might be rendering pixels from 0,0 to 1024,768, and source 1 might be rendering pixels from 1025,0 to 2048, 768. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff553945">DISPLAYCONFIG_PATH_INFO</a>
 

 

