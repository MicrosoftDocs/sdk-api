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

# _DD_NONLOCALVIDMEMCAPS structure


## -description


The DD_NONLOCALVIDMEMCAPS structure contains the capabilities for nonlocal display memory.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DD_NONLOCALVIDMEMCAPS structure.


### -field dwNLVBCaps

Contains the driver-specific capabilities for nonlocal-to-local display memory blits. See the Remarks section for more information.


### -field dwNLVBCaps2

Contains more of the driver-specific capabilities for nonlocal-to-local display memory blits. See the Remarks section for more information.


### -field dwNLVBCKeyCaps

Contains driver color key capabilities for nonlocal-to-local display memory blits. See the Remarks section for more information.


### -field dwNLVBFXCaps

Contains driver FX capabilities for nonlocal-to-local display memory blits. See the Remarks section for more information.


### -field dwNLVBRops

Specifies an array of DD_ROP_SPACE DWORDs containing the raster operations supported for nonlocal-to-local blits. The constant DD_ROP_SPACE is defined in <i>ddraw.h</i>. See the Remarks section for more information.


## -remarks



On Microsoft Windows 2000 and later versions, the data structure is called DD_NONLOCALVIDMEMCAPS and on Windows 98/Me the data structure is called DDNONLOCALVIDMEMCAPS.

Normally, the <b>dwNLVBCaps</b>, <b>dwNLVBCaps2</b>, <b>dwNFLBCKeyCaps</b>, <b>dwNLVBFXCaps</b>, and <b>dwNLVBRops</b> members contain a subset of the flags used in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549248">DDCORECAPS</a> structure that is relevant to nonlocal-to-local blitting. However, to allow flexibility for device driver writers, any of the flags in DDCORECAPS can be used. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549248">DDCORECAPS</a>
 

 

