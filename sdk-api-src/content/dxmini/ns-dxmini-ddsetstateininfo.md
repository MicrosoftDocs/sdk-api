---
UID: NS:dxmini._DDSETSTATEININFO
title: DDSETSTATEININFO (dxmini.h)
author: windows-sdk-content
description: The DDSETSTATEININFO structure contains the surface and video port extensions (VPE) object information.
old-location: display\ddsetstateininfo.htm
tech.root: display
ms.assetid: 85fdf0eb-3253-4370-b1b5-ade85c5c992f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDDSETSTATEININFO, DDSETSTATEININFO, DDSETSTATEININFO structure [Display Devices], PDDSETSTATEININFO, PDDSETSTATEININFO structure pointer [Display Devices], Video_Structs_ac2e1c06-be26-4f4c-8dd9-e322535c3a12.xml, display.ddsetstateininfo, dxmini/DDSETSTATEININFO, dxmini/PDDSETSTATEININFO"
ms.topic: struct
f1_keywords: 
 - "dxmini/DDSETSTATEININFO"
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
ms.custom: 19H1
---

# DDSETSTATEININFO structure


## -description


The DDSETSTATEININFO structure contains the surface and <a href="https://docs.microsoft.com/windows-hardware/drivers/">video port extensions (VPE)</a> object information. 


## -struct-fields




### -field lpSurfaceData

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-_ddsurfacedata">DDSURFACEDATA</a> structure that contains the surface information. 


### -field lpVideoPortData

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddvideoportdata">DDVIDEOPORTDATA</a> structure that contains the VPE object information.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-_ddsurfacedata">DDSURFACEDATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxmini/ns-dxmini-ddvideoportdata">DDVIDEOPORTDATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxmini/nc-dxmini-pdx_setstate">DxSetState</a>
 

 

