---
UID: NS:dxmini._DDGETPREVIOUSAUTOFLIPOUTINFO
title: "_DDGETPREVIOUSAUTOFLIPOUTINFO"
author: windows-sdk-content
description: The DDGETPREVIOUSAUTOFLIPOUTINFO structure provides the surface data.
old-location: display\ddgetpreviousautoflipoutinfo.htm
tech.root: display
ms.assetid: 3009425c-00ba-4be5-be81-65905abf4a2a
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: "*PDDGETPREVIOUSAUTOFLIPOUTINFO, DDGETPREVIOUSAUTOFLIPOUTINFO, DDGETPREVIOUSAUTOFLIPOUTINFO structure [Display Devices], PDDGETPREVIOUSAUTOFLIPOUTINFO, PDDGETPREVIOUSAUTOFLIPOUTINFO structure pointer [Display Devices], Video_Structs_baf54add-b6fa-4f0b-8236-8fe6c0fc95b6.xml, _DDGETPREVIOUSAUTOFLIPOUTINFO, display.ddgetpreviousautoflipoutinfo, dxmini/DDGETPREVIOUSAUTOFLIPOUTINFO, dxmini/PDDGETPREVIOUSAUTOFLIPOUTINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDGETPREVIOUSAUTOFLIPOUTINFO
product: Windows
targetos: Windows
req.typenames: DDGETPREVIOUSAUTOFLIPOUTINFO, *PDDGETPREVIOUSAUTOFLIPOUTINFO
req.redist: 
---

# _DDGETPREVIOUSAUTOFLIPOUTINFO structure


## -description


The DDGETPREVIOUSAUTOFLIPOUTINFO structure provides the surface data. 


## -struct-fields




### -field dwSurfaceIndex

Specifies the current zero-based index in the autoflip chain of the current surface. 


### -field dwVBISurfaceIndex

Specifies the current zero-based index in the autoflip chain of the current <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">vertical blanking interval (VBI)</a> surface. 


## -see-also




<a href="https://msdn.microsoft.com/3b19e4be-413c-4014-b414-cb2ba3e14b14">DxGetPreviousAutoflip</a>
 

 

