---
UID: NS:wingdi.DISPLAYCONFIG_PATH_INFO
title: DISPLAYCONFIG_PATH_INFO
author: windows-sdk-content
description: The DISPLAYCONFIG_PATH_INFO structure is used to describe a single path from a target to a source.
old-location: display\displayconfig_path_info.htm
old-project: display
ms.assetid: e218c36d-60d5-42c8-9443-419a388a2b8d
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: CCD_Structures_2953f0bc-d985-40e0-894d-9fe2593061ed.xml, DISPLAYCONFIG_PATH_INFO, DISPLAYCONFIG_PATH_INFO structure [Display Devices], display.displayconfig_path_info, wingdi/DISPLAYCONFIG_PATH_INFO
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
tech.root: 
req.typenames: DISPLAYCONFIG_PATH_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_PATH_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

