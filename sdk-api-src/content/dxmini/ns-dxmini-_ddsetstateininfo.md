---
UID: NS:dxmini._DDSETSTATEININFO
title: "_DDSETSTATEININFO"
author: windows-sdk-content
description: The DDSETSTATEININFO structure contains the surface and video port extensions (VPE) object information.
old-location: display\ddsetstateininfo.htm
tech.root: Display
ms.assetid: 85fdf0eb-3253-4370-b1b5-ade85c5c992f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDDSETSTATEININFO, DDSETSTATEININFO, DDSETSTATEININFO structure [Display Devices], PDDSETSTATEININFO, PDDSETSTATEININFO structure pointer [Display Devices], Video_Structs_ac2e1c06-be26-4f4c-8dd9-e322535c3a12.xml, _DDSETSTATEININFO, display.ddsetstateininfo, dxmini/DDSETSTATEININFO, dxmini/PDDSETSTATEININFO"
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
 - DDSETSTATEININFO
product: Windows
targetos: Windows
req.typenames: DDSETSTATEININFO, *PDDSETSTATEININFO
req.redist: 
---

# _DDSETSTATEININFO structure


## -description


The DDSETSTATEININFO structure contains the surface and <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object information. 


## -struct-fields




### -field lpSurfaceData

Points to a <a href="https://msdn.microsoft.com/4057cfcf-675e-439f-8b51-23adede1d35a">DDSURFACEDATA</a> structure that contains the surface information. 


### -field lpVideoPortData

Points to a <a href="https://msdn.microsoft.com/662ff6ee-d6b1-4cb1-8ff8-b4c1e17b26df">DDVIDEOPORTDATA</a> structure that contains the VPE object information.


## -see-also




<a href="https://msdn.microsoft.com/4057cfcf-675e-439f-8b51-23adede1d35a">DDSURFACEDATA</a>



<a href="https://msdn.microsoft.com/662ff6ee-d6b1-4cb1-8ff8-b4c1e17b26df">DDVIDEOPORTDATA</a>



<a href="https://msdn.microsoft.com/f2d7f248-017e-4375-b0a0-49de65192511">DxSetState</a>
 

 

