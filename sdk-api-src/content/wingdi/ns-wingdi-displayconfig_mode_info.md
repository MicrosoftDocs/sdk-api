---
UID: NS:wingdi.DISPLAYCONFIG_MODE_INFO
title: DISPLAYCONFIG_MODE_INFO
author: windows-sdk-content
description: The DISPLAYCONFIG_MODE_INFO structure contains either source mode or target mode information.
old-location: display\displayconfig_mode_info.htm
tech.root: display
ms.assetid: 39ffe49b-96d3-4d8b-94a7-01c388448b82
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CCD_Structures_e1d7b2cb-4d20-49d7-8eef-53ef7e369293.xml, DISPLAYCONFIG_MODE_INFO, DISPLAYCONFIG_MODE_INFO structure [Display Devices], display.displayconfig_mode_info, wingdi/DISPLAYCONFIG_MODE_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_MODE_INFO
product: Windows
targetos: Windows
req.typenames: DISPLAYCONFIG_MODE_INFO
req.redist: 
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

A valid <a href="https://msdn.microsoft.com/c81768f0-67d3-4ddd-94c8-013b1e4cf83e">DISPLAYCONFIG_TARGET_MODE</a> structure that describes the specified target only when <b>infoType</b> is DISPLAYCONFIG_MODE_INFO_TYPE_TARGET.


### -field DUMMYUNIONNAME.sourceMode

A valid <a href="https://msdn.microsoft.com/413d63e5-da9d-4906-80a9-049da6e85275">DISPLAYCONFIG_SOURCE_MODE</a> structure that describes the specified source only when <b>infoType</b> is DISPLAYCONFIG_MODE_INFO_TYPE_SOURCE.


### -field DUMMYUNIONNAME.desktopImageInfo

A <a href="https://msdn.microsoft.com/2DACA175-19BC-4192-A2FF-CB8AC7220B98">DISPLAYCONFIG_DESKTOP_IMAGE_INFO</a> structure that describes information about the desktop image only when <b>infoType</b> is DISPLAYCONFIG_MODE_INFO_TYPE_. 

Supported starting in Windows 10.


## -see-also




<a href="https://msdn.microsoft.com/d5ddb1d5-6b74-471f-86f0-fee72f30b648">DISPLAYCONFIG_MODE_INFO_TYPE</a>



<a href="https://msdn.microsoft.com/413d63e5-da9d-4906-80a9-049da6e85275">DISPLAYCONFIG_SOURCE_MODE</a>



<a href="https://msdn.microsoft.com/c81768f0-67d3-4ddd-94c8-013b1e4cf83e">DISPLAYCONFIG_TARGET_MODE</a>
 

 

