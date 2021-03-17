---
UID: NS:dxmini._DDGETIRQINFO
title: DDGETIRQINFO (dxmini.h)
description: The DDGETIRQINFO structure contains interrupt information for the video miniport driver.
helpviewer_keywords: ["*PDDGETIRQINFO","DDGETIRQINFO","DDGETIRQINFO structure [Display Devices]","PDDGETIRQINFO","PDDGETIRQINFO structure pointer [Display Devices]","Video_Structs_18f717ac-c026-4679-b55f-394135132ccc.xml","display.ddgetirqinfo","dxmini/DDGETIRQINFO","dxmini/PDDGETIRQINFO"]
old-location: display\ddgetirqinfo.htm
tech.root: display
ms.assetid: fdc3b929-902b-4759-b603-1624e3fb01dc
ms.date: 12/05/2018
ms.keywords: '*PDDGETIRQINFO, DDGETIRQINFO, DDGETIRQINFO structure [Display Devices], PDDGETIRQINFO, PDDGETIRQINFO structure pointer [Display Devices], Video_Structs_18f717ac-c026-4679-b55f-394135132ccc.xml, display.ddgetirqinfo, dxmini/DDGETIRQINFO, dxmini/PDDGETIRQINFO'
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
req.typenames: DDGETIRQINFO, *PDDGETIRQINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGETIRQINFO
 - dxmini/_DDGETIRQINFO
 - PDDGETIRQINFO
 - dxmini/PDDGETIRQINFO
 - DDGETIRQINFO
 - dxmini/DDGETIRQINFO
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
 - DDGETIRQINFO
---

# DDGETIRQINFO structure


## -description

The DDGETIRQINFO structure contains interrupt information for the video miniport driver.

## -struct-fields

### -field dwFlags

Specifies the interrupt management status.





#### IRQINFO_HANDLED

The video miniport driver is managing the interrupt.

## -see-also

<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_getirqinfo">DxGetIRQInfo</a>