---
UID: NS:wingdi.tagEMRCREATEPEN
title: EMRCREATEPEN (wingdi.h)
description: The EMRCREATEPEN structure contains members for the CreatePen enhanced metafile record.
helpviewer_keywords: ["*PEMRCREATEPEN","EMRCREATEPEN","EMRCREATEPEN structure [Windows GDI]","PEMRCREATEPEN","PEMRCREATEPEN structure pointer [Windows GDI]","_win32_EMRCREATEPEN_str","gdi.emrcreatepen","wingdi/EMRCREATEPEN","wingdi/PEMRCREATEPEN"]
old-location: gdi\emrcreatepen.htm
tech.root: gdi
ms.assetid: bd338c56-00b4-4eae-9e4f-57ac49809f32
ms.date: 12/05/2018
ms.keywords: '*PEMRCREATEPEN, EMRCREATEPEN, EMRCREATEPEN structure [Windows GDI], PEMRCREATEPEN, PEMRCREATEPEN structure pointer [Windows GDI], _win32_EMRCREATEPEN_str, gdi.emrcreatepen, wingdi/EMRCREATEPEN, wingdi/PEMRCREATEPEN'
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
req.typenames: EMRCREATEPEN, *PEMRCREATEPEN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRCREATEPEN
 - wingdi/tagEMRCREATEPEN
 - PEMRCREATEPEN
 - wingdi/PEMRCREATEPEN
 - EMRCREATEPEN
 - wingdi/EMRCREATEPEN
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
 - EMRCREATEPEN
---

# EMRCREATEPEN structure


## -description

The <b>EMRCREATEPEN</b> structure contains members for the <b>CreatePen</b> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ihPen

Index to pen in handle table.

### -field lopn

Logical pen.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createpen">CreatePen</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>