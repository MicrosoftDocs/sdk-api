---
UID: NS:wingdi.tagEMRPIXELFORMAT
title: EMRPIXELFORMAT (wingdi.h)
description: The EMRPIXELFORMAT structure contains the members for the SetPixelFormat enhanced metafile record. The pixel format information in ENHMETAHEADER refers to this structure.
helpviewer_keywords: ["*PEMRPIXELFORMAT","EMRPIXELFORMAT","EMRPIXELFORMAT structure [Windows GDI]","PEMRPIXELFORMAT","PEMRPIXELFORMAT structure pointer [Windows GDI]","_win32_EMRPIXELFORMAT_str","gdi.emrpixelformat","wingdi/EMRPIXELFORMAT","wingdi/PEMRPIXELFORMAT"]
old-location: gdi\emrpixelformat.htm
tech.root: gdi
ms.assetid: 3dd2ef54-af00-4d7e-b33f-c7c5160ae4f1
ms.date: 12/05/2018
ms.keywords: '*PEMRPIXELFORMAT, EMRPIXELFORMAT, EMRPIXELFORMAT structure [Windows GDI], PEMRPIXELFORMAT, PEMRPIXELFORMAT structure pointer [Windows GDI], _win32_EMRPIXELFORMAT_str, gdi.emrpixelformat, wingdi/EMRPIXELFORMAT, wingdi/PEMRPIXELFORMAT'
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
req.typenames: EMRPIXELFORMAT, *PEMRPIXELFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRPIXELFORMAT
 - wingdi/tagEMRPIXELFORMAT
 - PEMRPIXELFORMAT
 - wingdi/PEMRPIXELFORMAT
 - EMRPIXELFORMAT
 - wingdi/EMRPIXELFORMAT
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
 - EMRPIXELFORMAT
---

# EMRPIXELFORMAT structure


## -description

The <b>EMRPIXELFORMAT</b> structure contains the members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-setpixelformat">SetPixelFormat</a> enhanced metafile record. The pixel format information in <a href="/windows/desktop/api/wingdi/ns-wingdi-enhmetaheader">ENHMETAHEADER</a> refers to this structure.

## -struct-fields

### -field emr

The base structure for all record types.

### -field pfd

A 
            <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a> structure, which describes the pixel format.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-enhmetaheader">ENHMETAHEADER</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpixelformat">SetPixelFormat</a>