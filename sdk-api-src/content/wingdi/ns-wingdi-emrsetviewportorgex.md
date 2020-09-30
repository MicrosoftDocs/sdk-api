---
UID: NS:wingdi.tagEMRSETVIEWPORTORGEX
title: EMRSETVIEWPORTORGEX (wingdi.h)
description: The EMRSETVIEWPORTORGEX, EMRSETWINDOWORGEX, and EMRSETBRUSHORGEX structures contain members for the SetViewportOrgEx, SetWindowOrgEx, and SetBrushOrgEx enhanced metafile records.
helpviewer_keywords: ["*PEMRSETBRUSHORGEX","*PEMRSETVIEWPORTORGEX","*PEMRSETWINDOWORGEX","EMRSETBRUSHORGEX","EMRSETBRUSHORGEX structure [Windows GDI]","EMRSETVIEWPORTORGEX","EMRSETVIEWPORTORGEX structure [Windows GDI]","EMRSETVIEWPORTORGEX","EMRSETWINDOWORGEX","EMRSETBRUSHORGEX","EMRSETVIEWPORTORGEX","EMRSETWINDOWORGEX","EMRSETBRUSHORGEX structure [Windows GDI]","EMRSETWINDOWORGEX","EMRSETWINDOWORGEX structure [Windows GDI]","PEMRSETBRUSHORGEX","PEMRSETBRUSHORGEX structure pointer [Windows GDI]","PEMRSETVIEWPORTORGEX","PEMRSETVIEWPORTORGEX structure pointer [Windows GDI]","PEMRSETWINDOWORGEX","PEMRSETWINDOWORGEX structure pointer [Windows GDI]","_win32_EMRSETVIEWPORTORGEX_str","gdi.emrsetviewportorgex__emrsetwindoworgex__emrsetbrushorgex","wingdi/EMRSETBRUSHORGEX","wingdi/EMRSETVIEWPORTORGEX","EMRSETWINDOWORGEX","EMRSETBRUSHORGEX","wingdi/EMRSETWINDOWORGEX","wingdi/PEMRSETBRUSHORGEX","wingdi/PEMRSETVIEWPORTORGEX","wingdi/PEMRSETWINDOWORGEX"]
old-location: gdi\emrsetviewportorgex__emrsetwindoworgex__emrsetbrushorgex.htm
tech.root: gdi
ms.assetid: df80b89a-67b2-4ab3-8ff8-f121f9eb88cd
ms.date: 12/05/2018
ms.keywords: '*PEMRSETBRUSHORGEX, *PEMRSETVIEWPORTORGEX, *PEMRSETWINDOWORGEX, EMRSETBRUSHORGEX, EMRSETBRUSHORGEX structure [Windows GDI], EMRSETVIEWPORTORGEX, EMRSETVIEWPORTORGEX structure [Windows GDI], EMRSETVIEWPORTORGEX,EMRSETWINDOWORGEX,EMRSETBRUSHORGEX, EMRSETVIEWPORTORGEX,EMRSETWINDOWORGEX,EMRSETBRUSHORGEX structure [Windows GDI], EMRSETWINDOWORGEX, EMRSETWINDOWORGEX structure [Windows GDI], PEMRSETBRUSHORGEX, PEMRSETBRUSHORGEX structure pointer [Windows GDI], PEMRSETVIEWPORTORGEX, PEMRSETVIEWPORTORGEX structure pointer [Windows GDI], PEMRSETWINDOWORGEX, PEMRSETWINDOWORGEX structure pointer [Windows GDI], _win32_EMRSETVIEWPORTORGEX_str, gdi.emrsetviewportorgex__emrsetwindoworgex__emrsetbrushorgex, wingdi/EMRSETBRUSHORGEX, wingdi/EMRSETVIEWPORTORGEX,EMRSETWINDOWORGEX,EMRSETBRUSHORGEX, wingdi/EMRSETWINDOWORGEX, wingdi/PEMRSETBRUSHORGEX, wingdi/PEMRSETVIEWPORTORGEX, wingdi/PEMRSETWINDOWORGEX'
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
req.typenames: EMRSETVIEWPORTORGEX, *PEMRSETVIEWPORTORGEX, EMRSETWINDOWORGEX, *PEMRSETWINDOWORGEX, EMRSETBRUSHORGEX, *PEMRSETBRUSHORGEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSETVIEWPORTORGEX
 - wingdi/tagEMRSETVIEWPORTORGEX
 - PEMRSETVIEWPORTORGEX
 - wingdi/PEMRSETVIEWPORTORGEX
 - EMRSETVIEWPORTORGEX
 - wingdi/EMRSETVIEWPORTORGEX
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
 - EMRSETVIEWPORTORGEX
---

# EMRSETVIEWPORTORGEX structure


## -description

The <b>EMRSETVIEWPORTORGEX, </b><b>EMRSETWINDOWORGEX, </b> and <b>EMRSETBRUSHORGEX</b> structures contain members for the <b>SetViewportOrgEx</b>, <b>SetWindowOrgEx</b>, and <b>SetBrushOrgEx</b> enhanced metafile records.

## -struct-fields

### -field emr

Base structure for all record types.

### -field ptlOrigin

Coordinates of the origin. For <b>EMRSETVIEWPORTORGEX</b> and <b>EMRSETBRUSHORGEX</b>, this is in device units. For <b>EMRSETWINDOWORGEX</b>, this is in logical units.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbrushorgex">SetBrushOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportorgex">SetViewportOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwindoworgex">SetWindowOrgEx</a>