---
UID: NS:wingdi.tagEMRCREATECOLORSPACE
title: EMRCREATECOLORSPACE (wingdi.h)
description: The EMRCREATECOLORSPACE structure contains members for the CreateColorSpace enhanced metafile record.
helpviewer_keywords: ["*PEMRCREATECOLORSPACE","EMRCREATECOLORSPACE","EMRCREATECOLORSPACE structure [Windows GDI]","PEMRCREATECOLORSPACE","PEMRCREATECOLORSPACE structure pointer [Windows GDI]","_win32_EMRCREATECOLORSPACE_str","gdi.emrcreatecolorspace","wingdi/EMRCREATECOLORSPACE","wingdi/PEMRCREATECOLORSPACE"]
old-location: gdi\emrcreatecolorspace.htm
tech.root: gdi
ms.assetid: ee2e02bb-5bd2-460c-aefe-78a143c72ff6
ms.date: 12/05/2018
ms.keywords: '*PEMRCREATECOLORSPACE, EMRCREATECOLORSPACE, EMRCREATECOLORSPACE structure [Windows GDI], PEMRCREATECOLORSPACE, PEMRCREATECOLORSPACE structure pointer [Windows GDI], _win32_EMRCREATECOLORSPACE_str, gdi.emrcreatecolorspace, wingdi/EMRCREATECOLORSPACE, wingdi/PEMRCREATECOLORSPACE'
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
req.typenames: EMRCREATECOLORSPACE, *PEMRCREATECOLORSPACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRCREATECOLORSPACE
 - wingdi/tagEMRCREATECOLORSPACE
 - PEMRCREATECOLORSPACE
 - wingdi/PEMRCREATECOLORSPACE
 - EMRCREATECOLORSPACE
 - wingdi/EMRCREATECOLORSPACE
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
 - EMRCREATECOLORSPACE
---

# EMRCREATECOLORSPACE structure


## -description

The <b>EMRCREATECOLORSPACE</b> structure contains members for the <b>CreateColorSpace</b> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ihCS

The index of the color space in handle table.

### -field lcs

The logical color space.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-emrcreatecolorspace">CreateColorSpace</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-emrcreatecolorspacew">EMRCREATECOLORSPACEW</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logcolorspacea">LOGCOLORSPACE</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>