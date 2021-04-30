---
UID: NS:wingdi._RASTERIZER_STATUS
title: RASTERIZER_STATUS (wingdi.h)
description: The RASTERIZER_STATUS structure contains information about whether TrueType is installed. This structure is filled when an application calls the GetRasterizerCaps function.
helpviewer_keywords: ["*LPRASTERIZER_STATUS","LPRASTERIZER_STATUS","LPRASTERIZER_STATUS structure pointer [Windows GDI]","RASTERIZER_STATUS","RASTERIZER_STATUS structure [Windows GDI]","_win32_RASTERIZER_STATUS_str","gdi.rasterizer_status","wingdi/LPRASTERIZER_STATUS","wingdi/RASTERIZER_STATUS"]
old-location: gdi\rasterizer_status.htm
tech.root: gdi
ms.assetid: 40bb4b59-90a4-4780-ae5f-fef8a6fa62cb
ms.date: 12/05/2018
ms.keywords: '*LPRASTERIZER_STATUS, LPRASTERIZER_STATUS, LPRASTERIZER_STATUS structure pointer [Windows GDI], RASTERIZER_STATUS, RASTERIZER_STATUS structure [Windows GDI], _win32_RASTERIZER_STATUS_str, gdi.rasterizer_status, wingdi/LPRASTERIZER_STATUS, wingdi/RASTERIZER_STATUS'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: RASTERIZER_STATUS, *LPRASTERIZER_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RASTERIZER_STATUS
 - wingdi/_RASTERIZER_STATUS
 - LPRASTERIZER_STATUS
 - wingdi/LPRASTERIZER_STATUS
 - RASTERIZER_STATUS
 - wingdi/RASTERIZER_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - RASTERIZER_STATUS
---

# RASTERIZER_STATUS structure


## -description

The <b>RASTERIZER_STATUS</b> structure contains information about whether TrueType is installed. This structure is filled when an application calls the <a href="/windows/desktop/api/wingdi/nf-wingdi-getrasterizercaps">GetRasterizerCaps</a> function.

## -struct-fields

### -field nSize

The size, in bytes, of the <b>RASTERIZER_STATUS</b> structure.

### -field wFlags

Specifies whether at least one TrueType font is installed and whether TrueType is enabled. This value is TT_AVAILABLE, TT_ENABLED, or both if TrueType is on the system.

### -field nLanguageID

The language in the system's Setup.inf file.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getrasterizercaps">GetRasterizerCaps</a>