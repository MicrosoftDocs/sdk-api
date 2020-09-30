---
UID: NS:ddrawi._DDHAL_DESTROYDDLOCALDATA
title: DDHAL_DESTROYDDLOCALDATA (ddrawi.h)
description: DDHAL_DESTROYDDLOCALDATA contains the information required for the driver to destroy a set of surfaces associated to a given local DirectDraw object.
helpviewer_keywords: ["*LPDDHAL_DESTROYDDLOCALDATA","DDHAL_DESTROYDDLOCALDATA","DDHAL_DESTROYDDLOCALDATA structure [Display Devices]","d3dstrct_1c587282-0c7f-4a8a-90ce-199cca0e86b9.xml","ddrawi/DDHAL_DESTROYDDLOCALDATA","display.ddhal_destroyddlocaldata"]
old-location: display\ddhal_destroyddlocaldata.htm
tech.root: display
ms.assetid: 9d1d14b8-ceaf-4845-a388-a084aa0472a7
ms.date: 12/05/2018
ms.keywords: '*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA structure [Display Devices], d3dstrct_1c587282-0c7f-4a8a-90ce-199cca0e86b9.xml, ddrawi/DDHAL_DESTROYDDLOCALDATA, display.ddhal_destroyddlocaldata'
req.header: ddrawi.h
req.include-header: D3dhal.h
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
req.typenames: '*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDHAL_DESTROYDDLOCALDATA
 - ddrawi/_DDHAL_DESTROYDDLOCALDATA
 - LPDDHAL_DESTROYDDLOCALDATA
 - ddrawi/LPDDHAL_DESTROYDDLOCALDATA
 - DDHAL_DESTROYDDLOCALDATA
 - ddrawi/DDHAL_DESTROYDDLOCALDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawi.h
api_name:
 - DDHAL_DESTROYDDLOCALDATA
---

# DDHAL_DESTROYDDLOCALDATA structure


## -description

DDHAL_DESTROYDDLOCALDATA contains the information required for the driver to destroy a set of surfaces associated to a given local DirectDraw object.

## -struct-fields

### -field dwFlags

Unused.

### -field pDDLcl

Points to the local Direct Draw object that serves as a reference for all Direct3D surfaces that have to be destroyed.

### -field ddRVal

Specifies the location where the driver writes the return value of <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_destroyddlocal">D3dDestroyDDLocal</a>. A return code of D3D_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-codes-for-direct3d-driver-callbacks">Return Codes for Direct3D Driver Callbacks</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_destroyddlocal">D3dDestroyDDLocal</a>