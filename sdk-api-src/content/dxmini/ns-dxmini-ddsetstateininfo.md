---
UID: NS:dxmini._DDSETSTATEININFO
title: DDSETSTATEININFO (dxmini.h)
description: The DDSETSTATEININFO structure contains the surface and video port extensions (VPE) object information.
helpviewer_keywords: ["*PDDSETSTATEININFO","DDSETSTATEININFO","DDSETSTATEININFO structure [Display Devices]","PDDSETSTATEININFO","PDDSETSTATEININFO structure pointer [Display Devices]","Video_Structs_ac2e1c06-be26-4f4c-8dd9-e322535c3a12.xml","display.ddsetstateininfo","dxmini/DDSETSTATEININFO","dxmini/PDDSETSTATEININFO"]
old-location: display\ddsetstateininfo.htm
tech.root: display
ms.assetid: 85fdf0eb-3253-4370-b1b5-ade85c5c992f
ms.date: 12/05/2018
ms.keywords: '*PDDSETSTATEININFO, DDSETSTATEININFO, DDSETSTATEININFO structure [Display Devices], PDDSETSTATEININFO, PDDSETSTATEININFO structure pointer [Display Devices], Video_Structs_ac2e1c06-be26-4f4c-8dd9-e322535c3a12.xml, display.ddsetstateininfo, dxmini/DDSETSTATEININFO, dxmini/PDDSETSTATEININFO'
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
targetos: Windows
req.typenames: DDSETSTATEININFO, *PDDSETSTATEININFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDSETSTATEININFO
 - dxmini/_DDSETSTATEININFO
 - PDDSETSTATEININFO
 - dxmini/PDDSETSTATEININFO
 - DDSETSTATEININFO
 - dxmini/DDSETSTATEININFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDSETSTATEININFO
---

# DDSETSTATEININFO structure


## -description

The DDSETSTATEININFO structure contains the surface and <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object information.

## -struct-fields

### -field lpSurfaceData

Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddsurfacedata">DDSURFACEDATA</a> structure that contains the surface information.

### -field lpVideoPortData

Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddvideoportdata">DDVIDEOPORTDATA</a> structure that contains the VPE object information.

## -see-also

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddsurfacedata">DDSURFACEDATA</a>



<a href="/windows/desktop/api/dxmini/ns-dxmini-ddvideoportdata">DDVIDEOPORTDATA</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_setstate">DxSetState</a>