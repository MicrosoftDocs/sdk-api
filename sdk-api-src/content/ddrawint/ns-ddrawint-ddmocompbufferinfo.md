---
UID: NS:ddrawint._DDMOCOMPBUFFERINFO
title: DDMOCOMPBUFFERINFO (ddrawint.h)
description: The DDMOCOMPBUFFERINFO structure contains the macro block information required to render a frame and passes this information to the DD_RENDERMOCOMPDATA structure.
helpviewer_keywords: ["*LPDDMOCOMPBUFFERINFO","DDMOCOMPBUFFERINFO","DDMOCOMPBUFFERINFO structure [Display Devices]","LPDDMOCOMPBUFFERINFO","LPDDMOCOMPBUFFERINFO structure pointer [Display Devices]","ddrawint/DDMOCOMPBUFFERINFO","ddrawint/LPDDMOCOMPBUFFERINFO","ddstrcts_8716da01-eda5-4102-b881-c2e368f0792a.xml","display.ddmocompbufferinfo"]
old-location: display\ddmocompbufferinfo.htm
tech.root: display
ms.assetid: e039f85e-868f-4673-bbaa-9165bd760e9d
ms.date: 12/05/2018
ms.keywords: '*LPDDMOCOMPBUFFERINFO, DDMOCOMPBUFFERINFO, DDMOCOMPBUFFERINFO structure [Display Devices], LPDDMOCOMPBUFFERINFO, LPDDMOCOMPBUFFERINFO structure pointer [Display Devices], ddrawint/DDMOCOMPBUFFERINFO, ddrawint/LPDDMOCOMPBUFFERINFO, ddstrcts_8716da01-eda5-4102-b881-c2e368f0792a.xml, display.ddmocompbufferinfo'
req.header: ddrawint.h
req.include-header: Winddi.h
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
req.typenames: DDMOCOMPBUFFERINFO, *LPDDMOCOMPBUFFERINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDMOCOMPBUFFERINFO
 - ddrawint/_DDMOCOMPBUFFERINFO
 - LPDDMOCOMPBUFFERINFO
 - ddrawint/LPDDMOCOMPBUFFERINFO
 - DDMOCOMPBUFFERINFO
 - ddrawint/DDMOCOMPBUFFERINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DDMOCOMPBUFFERINFO
---

# DDMOCOMPBUFFERINFO structure


## -description

The DDMOCOMPBUFFERINFO structure contains the macro block information required to render a frame and passes this information to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_rendermocompdata">DD_RENDERMOCOMPDATA</a> structure.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DDMOCOMPBUFFERINFO structure.

### -field lpCompSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that contains the compressed data.

### -field dwDataOffset

Indicates the offset to the relevant data, in bytes, from the beginning of the buffer. This value does not allow for pitch.

### -field dwDataSize

Indicates the size of the relevant data in bytes. This value does not allow for pitch.

### -field lpPrivate

Used by Microsoft DirectDraw and should be ignored by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_rendermocompdata">DD_RENDERMOCOMPDATA</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a>