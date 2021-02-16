---
UID: NS:dxmini._DDLOCKOUTINFO
title: DDLOCKOUTINFO (dxmini.h)
description: The DDLOCKOUTINFO structure contains the surface information output from the DxLock function.
helpviewer_keywords: ["*PDDLOCKOUTINFO","DDLOCKOUTINFO","DDLOCKOUTINFO structure [Display Devices]","PDDLOCKOUTINFO","PDDLOCKOUTINFO structure pointer [Display Devices]","Video_Structs_7e32e28f-c3c0-48cc-85e7-341bed0382e5.xml","display.ddlockoutinfo","dxmini/DDLOCKOUTINFO","dxmini/PDDLOCKOUTINFO"]
old-location: display\ddlockoutinfo.htm
tech.root: display
ms.assetid: a29ec594-c5f9-46e4-a8c2-95e24e2ddb2d
ms.date: 12/05/2018
ms.keywords: '*PDDLOCKOUTINFO, DDLOCKOUTINFO, DDLOCKOUTINFO structure [Display Devices], PDDLOCKOUTINFO, PDDLOCKOUTINFO structure pointer [Display Devices], Video_Structs_7e32e28f-c3c0-48cc-85e7-341bed0382e5.xml, display.ddlockoutinfo, dxmini/DDLOCKOUTINFO, dxmini/PDDLOCKOUTINFO'
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
req.typenames: DDLOCKOUTINFO, *PDDLOCKOUTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDLOCKOUTINFO
 - dxmini/_DDLOCKOUTINFO
 - PDDLOCKOUTINFO
 - dxmini/PDDLOCKOUTINFO
 - DDLOCKOUTINFO
 - dxmini/DDLOCKOUTINFO
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
 - DDLOCKOUTINFO
---

# DDLOCKOUTINFO structure


## -description

The DDLOCKOUTINFO structure contains the surface information output from the <a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_lock">DxLock</a> function.

## -struct-fields

### -field dwSurfacePtr

Points to the surface in the frame buffer.

## -see-also

<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_lock">DxLock</a>