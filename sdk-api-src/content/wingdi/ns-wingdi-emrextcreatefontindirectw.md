---
UID: NS:wingdi.tagEMREXTCREATEFONTINDIRECTW
title: EMREXTCREATEFONTINDIRECTW (wingdi.h)
description: The EMREXTCREATEFONTINDIRECTW structure contains members for the CreateFontIndirect enhanced metafile record.
helpviewer_keywords: ["*PEMREXTCREATEFONTINDIRECTW","*PEMREXTCREATEFONTINDIRECTW structure [Windows GDI]","EMREXTCREATEFONTINDIRECTW","EMREXTCREATEFONTINDIRECTW structure [Windows GDI]","_win32_EMREXTCREATEFONTINDIRECTW_str","gdi.emrextcreatefontindirectw","wingdi/*PEMREXTCREATEFONTINDIRECTW","wingdi/EMREXTCREATEFONTINDIRECTW"]
old-location: gdi\emrextcreatefontindirectw.htm
tech.root: gdi
ms.assetid: 27adba1d-6845-4d5e-8183-9c092775b473
ms.date: 12/05/2018
ms.keywords: '*PEMREXTCREATEFONTINDIRECTW, *PEMREXTCREATEFONTINDIRECTW structure [Windows GDI], EMREXTCREATEFONTINDIRECTW, EMREXTCREATEFONTINDIRECTW structure [Windows GDI], _win32_EMREXTCREATEFONTINDIRECTW_str, gdi.emrextcreatefontindirectw, wingdi/*PEMREXTCREATEFONTINDIRECTW, wingdi/EMREXTCREATEFONTINDIRECTW'
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
req.typenames: EMREXTCREATEFONTINDIRECTW, *PEMREXTCREATEFONTINDIRECTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMREXTCREATEFONTINDIRECTW
 - wingdi/tagEMREXTCREATEFONTINDIRECTW
 - PEMREXTCREATEFONTINDIRECTW
 - wingdi/PEMREXTCREATEFONTINDIRECTW
 - EMREXTCREATEFONTINDIRECTW
 - wingdi/EMREXTCREATEFONTINDIRECTW
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
 - EMREXTCREATEFONTINDIRECTW
---

# EMREXTCREATEFONTINDIRECTW structure


## -description

The <b>EMREXTCREATEFONTINDIRECTW</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta">CreateFontIndirect</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ihFont

Index to the font in handle table.

### -field elfw

Logical font.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta">CreateFontIndirect</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>