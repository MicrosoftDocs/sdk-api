---
UID: NS:dxmini._DDGETPREVIOUSAUTOFLIPOUTINFO
title: DDGETPREVIOUSAUTOFLIPOUTINFO (dxmini.h)
description: The DDGETPREVIOUSAUTOFLIPOUTINFO structure provides the surface data.
helpviewer_keywords: ["*PDDGETPREVIOUSAUTOFLIPOUTINFO","DDGETPREVIOUSAUTOFLIPOUTINFO","DDGETPREVIOUSAUTOFLIPOUTINFO structure [Display Devices]","PDDGETPREVIOUSAUTOFLIPOUTINFO","PDDGETPREVIOUSAUTOFLIPOUTINFO structure pointer [Display Devices]","Video_Structs_baf54add-b6fa-4f0b-8236-8fe6c0fc95b6.xml","display.ddgetpreviousautoflipoutinfo","dxmini/DDGETPREVIOUSAUTOFLIPOUTINFO","dxmini/PDDGETPREVIOUSAUTOFLIPOUTINFO"]
old-location: display\ddgetpreviousautoflipoutinfo.htm
tech.root: display
ms.assetid: 3009425c-00ba-4be5-be81-65905abf4a2a
ms.date: 12/05/2018
ms.keywords: '*PDDGETPREVIOUSAUTOFLIPOUTINFO, DDGETPREVIOUSAUTOFLIPOUTINFO, DDGETPREVIOUSAUTOFLIPOUTINFO structure [Display Devices], PDDGETPREVIOUSAUTOFLIPOUTINFO, PDDGETPREVIOUSAUTOFLIPOUTINFO structure pointer [Display Devices], Video_Structs_baf54add-b6fa-4f0b-8236-8fe6c0fc95b6.xml, display.ddgetpreviousautoflipoutinfo, dxmini/DDGETPREVIOUSAUTOFLIPOUTINFO, dxmini/PDDGETPREVIOUSAUTOFLIPOUTINFO'
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
req.typenames: DDGETPREVIOUSAUTOFLIPOUTINFO, *PDDGETPREVIOUSAUTOFLIPOUTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGETPREVIOUSAUTOFLIPOUTINFO
 - dxmini/_DDGETPREVIOUSAUTOFLIPOUTINFO
 - PDDGETPREVIOUSAUTOFLIPOUTINFO
 - dxmini/PDDGETPREVIOUSAUTOFLIPOUTINFO
 - DDGETPREVIOUSAUTOFLIPOUTINFO
 - dxmini/DDGETPREVIOUSAUTOFLIPOUTINFO
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
 - DDGETPREVIOUSAUTOFLIPOUTINFO
---

# DDGETPREVIOUSAUTOFLIPOUTINFO structure


## -description

The DDGETPREVIOUSAUTOFLIPOUTINFO structure provides the surface data.

## -struct-fields

### -field dwSurfaceIndex

Specifies the current zero-based index in the autoflip chain of the current surface.

### -field dwVBISurfaceIndex

Specifies the current zero-based index in the autoflip chain of the current <a href="/windows-hardware/drivers/">vertical blanking interval (VBI)</a> surface.

## -see-also

<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_getpreviousautoflip">DxGetPreviousAutoflip</a>