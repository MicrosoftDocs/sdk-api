---
UID: NS:wingdi.DISPLAYCONFIG_PATH_INFO
title: DISPLAYCONFIG_PATH_INFO (wingdi.h)
author: windows-sdk-content
description: The DISPLAYCONFIG_PATH_INFO structure is used to describe a single path from a target to a source.
old-location: display\displayconfig_path_info.htm
tech.root: display
ms.assetid: e218c36d-60d5-42c8-9443-419a388a2b8d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CCD_Structures_2953f0bc-d985-40e0-894d-9fe2593061ed.xml, DISPLAYCONFIG_PATH_INFO, DISPLAYCONFIG_PATH_INFO structure [Display Devices], display.displayconfig_path_info, wingdi/DISPLAYCONFIG_PATH_INFO
ms.topic: struct
f1_keywords: 
 - "wingdi/DISPLAYCONFIG_PATH_INFO"
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
 - DISPLAYCONFIG_PATH_INFO
product: Windows
targetos: Windows
req.typenames: DISPLAYCONFIG_PATH_INFO
req.redist: 
ms.custom: 19H1
---

# DISPLAYCONFIG_PATH_INFO structure


## -description


The DISPLAYCONFIG_PATH_INFO structure is used to describe a single path from a target to a source.


## -struct-fields




### -field sourceInfo

A <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_source_info">DISPLAYCONFIG_PATH_SOURCE_INFO</a> structure that contains the source information for the path.


### -field targetInfo

A <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a> structure that contains the target information for the path.


### -field flags

A bitwise OR of flag values that indicates the state of the path. The following values are supported:





#### DISPLAYCONFIG_PATH_ACTIVE

Set by <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a> to indicate that the path is active and part of the desktop. If this flag value is set, <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a> attempts to enable this path.



#### DISPLAYCONFIG_PATH_SUPPORT_VIRTUAL_MODE

Set by <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a> to indicate that the path supports the virtual mode. Supported starting in Windows 10.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_source_info">DISPLAYCONFIG_PATH_SOURCE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-displayconfig_path_target_info">DISPLAYCONFIG_PATH_TARGET_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-querydisplayconfig">QueryDisplayConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setdisplayconfig">SetDisplayConfig</a>
 

 

