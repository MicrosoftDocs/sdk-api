---
UID: NS:dxmini._DDGETCURRENTAUTOFLIPOUTINFO
title: DDGETCURRENTAUTOFLIPOUTINFO (dxmini.h)
description: The DDGETCURRENTAUTOFLIPOUTINFO structure provides the surface information.
helpviewer_keywords: ["*PDDGETCURRENTAUTOFLIPOUTINFO","DDGETCURRENTAUTOFLIPOUTINFO","DDGETCURRENTAUTOFLIPOUTINFO structure [Display Devices]","PDDGETCURRENTAUTOFLIPOUTINFO","PDDGETCURRENTAUTOFLIPOUTINFO structure pointer [Display Devices]","Video_Structs_2e52113e-1796-45bf-bd0b-d0e373679f15.xml","display.ddgetcurrentautoflipoutinfo","dxmini/DDGETCURRENTAUTOFLIPOUTINFO","dxmini/PDDGETCURRENTAUTOFLIPOUTINFO"]
old-location: display\ddgetcurrentautoflipoutinfo.htm
tech.root: display
ms.assetid: 2dea32ab-9f4a-4184-9979-1103f1b26730
ms.date: 12/05/2018
ms.keywords: '*PDDGETCURRENTAUTOFLIPOUTINFO, DDGETCURRENTAUTOFLIPOUTINFO, DDGETCURRENTAUTOFLIPOUTINFO structure [Display Devices], PDDGETCURRENTAUTOFLIPOUTINFO, PDDGETCURRENTAUTOFLIPOUTINFO structure pointer [Display Devices], Video_Structs_2e52113e-1796-45bf-bd0b-d0e373679f15.xml, display.ddgetcurrentautoflipoutinfo, dxmini/DDGETCURRENTAUTOFLIPOUTINFO, dxmini/PDDGETCURRENTAUTOFLIPOUTINFO'
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
req.typenames: DDGETCURRENTAUTOFLIPOUTINFO, *PDDGETCURRENTAUTOFLIPOUTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGETCURRENTAUTOFLIPOUTINFO
 - dxmini/_DDGETCURRENTAUTOFLIPOUTINFO
 - PDDGETCURRENTAUTOFLIPOUTINFO
 - dxmini/PDDGETCURRENTAUTOFLIPOUTINFO
 - DDGETCURRENTAUTOFLIPOUTINFO
 - dxmini/DDGETCURRENTAUTOFLIPOUTINFO
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
 - DDGETCURRENTAUTOFLIPOUTINFO
---

# DDGETCURRENTAUTOFLIPOUTINFO structure


## -description

The DDGETCURRENTAUTOFLIPOUTINFO structure provides the surface information.

## -struct-fields

### -field dwSurfaceIndex

Specifies the current zero-based index in the autoflip chain of the current surface.

### -field dwVBISurfaceIndex

Specifies the current zero-based index in the autoflip chain of the current <a href="/windows-hardware/drivers/">vertical blanking interval (VBI)</a> surface.

## -see-also

<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_getcurrentautoflip">DxGetCurrentAutoflip</a>