---
UID: NS:wingdi.tagEMRELLIPSE
title: EMRELLIPSE (wingdi.h)
description: The EMRELLIPSE and EMRRECTANGLE structures contain members for the Ellipse and Rectangle enhanced metafile records.
helpviewer_keywords: ["*PEMRELLIPSE","*PEMRRECTANGLE","EMRELLIPSE","EMRELLIPSE structure [Windows GDI]","EMRELLIPSE","EMRRECTANGLE","EMRELLIPSE","EMRRECTANGLE structure [Windows GDI]","EMRRECTANGLE","EMRRECTANGLE structure [Windows GDI]","PEMRELLIPSE","PEMRELLIPSE structure pointer [Windows GDI]","PEMRRECTANGLE","PEMRRECTANGLE structure pointer [Windows GDI]","_win32_EMRELLIPSE_str","gdi.emrellipse__emrrectangle","wingdi/EMRELLIPSE","EMRRECTANGLE","wingdi/EMRRECTANGLE","wingdi/PEMRELLIPSE","wingdi/PEMRRECTANGLE"]
old-location: gdi\emrellipse__emrrectangle.htm
tech.root: gdi
ms.assetid: 1400f9d7-4ccd-4348-98f0-fccc78e06212
ms.date: 12/05/2018
ms.keywords: '*PEMRELLIPSE, *PEMRRECTANGLE, EMRELLIPSE, EMRELLIPSE structure [Windows GDI], EMRELLIPSE,EMRRECTANGLE, EMRELLIPSE,EMRRECTANGLE structure [Windows GDI], EMRRECTANGLE, EMRRECTANGLE structure [Windows GDI], PEMRELLIPSE, PEMRELLIPSE structure pointer [Windows GDI], PEMRRECTANGLE, PEMRRECTANGLE structure pointer [Windows GDI], _win32_EMRELLIPSE_str, gdi.emrellipse__emrrectangle, wingdi/EMRELLIPSE,EMRRECTANGLE, wingdi/EMRRECTANGLE, wingdi/PEMRELLIPSE, wingdi/PEMRRECTANGLE'
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
req.typenames: EMRELLIPSE, *PEMRELLIPSE, EMRRECTANGLE, *PEMRRECTANGLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRELLIPSE
 - wingdi/tagEMRELLIPSE
 - PEMRELLIPSE
 - wingdi/PEMRELLIPSE
 - EMRELLIPSE
 - wingdi/EMRELLIPSE
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
 - EMRELLIPSE
---

# EMRELLIPSE structure


## -description

The <b>EMRELLIPSE</b> and <b>EMRRECTANGLE</b> structures contain members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-ellipse">Ellipse</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-rectangle">Rectangle</a> enhanced metafile records.

## -struct-fields

### -field emr

Base structure for all record types.

### -field rclBox

Bounding rectangle in logical units.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-ellipse">Ellipse</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rectangle">Rectangle</a>