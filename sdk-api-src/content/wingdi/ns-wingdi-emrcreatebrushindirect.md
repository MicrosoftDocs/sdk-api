---
UID: NS:wingdi.tagEMRCREATEBRUSHINDIRECT
title: EMRCREATEBRUSHINDIRECT (wingdi.h)
description: The EMRCREATEBRUSHINDIRECT structure contains members for the CreateBrushIndirect enhanced metafile record.
helpviewer_keywords: ["*PEMRCREATEBRUSHINDIRECT","EMRCREATEBRUSHINDIRECT","EMRCREATEBRUSHINDIRECT structure [Windows GDI]","PEMRCREATEBRUSHINDIRECT","PEMRCREATEBRUSHINDIRECT structure pointer [Windows GDI]","_win32_EMRCREATEBRUSHINDIRECT_str","gdi.emrcreatebrushindirect","wingdi/EMRCREATEBRUSHINDIRECT","wingdi/PEMRCREATEBRUSHINDIRECT"]
old-location: gdi\emrcreatebrushindirect.htm
tech.root: gdi
ms.assetid: fd87d52a-1227-48ba-8b7e-a8fd007c9d01
ms.date: 12/05/2018
ms.keywords: '*PEMRCREATEBRUSHINDIRECT, EMRCREATEBRUSHINDIRECT, EMRCREATEBRUSHINDIRECT structure [Windows GDI], PEMRCREATEBRUSHINDIRECT, PEMRCREATEBRUSHINDIRECT structure pointer [Windows GDI], _win32_EMRCREATEBRUSHINDIRECT_str, gdi.emrcreatebrushindirect, wingdi/EMRCREATEBRUSHINDIRECT, wingdi/PEMRCREATEBRUSHINDIRECT'
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
req.typenames: EMRCREATEBRUSHINDIRECT, *PEMRCREATEBRUSHINDIRECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRCREATEBRUSHINDIRECT
 - wingdi/tagEMRCREATEBRUSHINDIRECT
 - PEMRCREATEBRUSHINDIRECT
 - wingdi/PEMRCREATEBRUSHINDIRECT
 - EMRCREATEBRUSHINDIRECT
 - wingdi/EMRCREATEBRUSHINDIRECT
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
 - EMRCREATEBRUSHINDIRECT
---

# EMRCREATEBRUSHINDIRECT structure


## -description

The <b>EMRCREATEBRUSHINDIRECT</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect">CreateBrushIndirect</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ihBrush

Index of brush in handle table.

### -field lb

A <a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush32">LOGBRUSH32</a> structure containing information about the brush. The <b>lbStyle</b> member must be either the BS_SOLID, BS_HOLLOW, BS_NULL, or BS_HATCHED value.

Note, that if your code is used on both 32-bit and 64-bit platforms, you must use the <a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush32">LOGBRUSH32</a> structure. This maintains compatibility between the platforms when you record the metafile on one platform and use it on the other platform. If your code remains on one platform, it is sufficient to use <a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush">LOGBRUSH</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect">CreateBrushIndirect</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush">LOGBRUSH</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush32">LOGBRUSH32</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>