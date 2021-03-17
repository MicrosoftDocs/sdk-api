---
UID: NS:wingdi.tagEMREXTTEXTOUTA
title: EMREXTTEXTOUTA (wingdi.h)
description: The EMREXTTEXTOUTA and EMREXTTEXTOUTW structures contain members for the ExtTextOut, TextOut, or DrawText enhanced metafile records.
helpviewer_keywords: ["*PEMREXTTEXTOUTA","*PEMREXTTEXTOUTW","EMREXTTEXTOUTA","EMREXTTEXTOUTA structure [Windows GDI]","EMREXTTEXTOUTA","EMREXTTEXTOUTW","EMREXTTEXTOUTA","EMREXTTEXTOUTW structure [Windows GDI]","EMREXTTEXTOUTW","EMREXTTEXTOUTW structure [Windows GDI]","PEMREXTTEXTOUTA","PEMREXTTEXTOUTA structure pointer [Windows GDI]","PEMREXTTEXTOUTW","PEMREXTTEXTOUTW structure pointer [Windows GDI]","_win32_EMREXTTEXTOUTA_str","gdi.emrexttextouta__emrexttextoutw","wingdi/EMREXTTEXTOUTA","EMREXTTEXTOUTW","wingdi/EMREXTTEXTOUTW","wingdi/PEMREXTTEXTOUTA","wingdi/PEMREXTTEXTOUTW"]
old-location: gdi\emrexttextouta__emrexttextoutw.htm
tech.root: gdi
ms.assetid: 1d9b0b32-6a51-481a-9589-3de832d746d7
ms.date: 12/05/2018
ms.keywords: '*PEMREXTTEXTOUTA, *PEMREXTTEXTOUTW, EMREXTTEXTOUTA, EMREXTTEXTOUTA structure [Windows GDI], EMREXTTEXTOUTA,EMREXTTEXTOUTW, EMREXTTEXTOUTA,EMREXTTEXTOUTW structure [Windows GDI], EMREXTTEXTOUTW, EMREXTTEXTOUTW structure [Windows GDI], PEMREXTTEXTOUTA, PEMREXTTEXTOUTA structure pointer [Windows GDI], PEMREXTTEXTOUTW, PEMREXTTEXTOUTW structure pointer [Windows GDI], _win32_EMREXTTEXTOUTA_str, gdi.emrexttextouta__emrexttextoutw, wingdi/EMREXTTEXTOUTA,EMREXTTEXTOUTW, wingdi/EMREXTTEXTOUTW, wingdi/PEMREXTTEXTOUTA, wingdi/PEMREXTTEXTOUTW'
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
req.typenames: EMREXTTEXTOUTA, *PEMREXTTEXTOUTA, EMREXTTEXTOUTW, *PEMREXTTEXTOUTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMREXTTEXTOUTA
 - wingdi/tagEMREXTTEXTOUTA
 - PEMREXTTEXTOUTA
 - wingdi/PEMREXTTEXTOUTA
 - EMREXTTEXTOUTA
 - wingdi/EMREXTTEXTOUTA
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
 - EMREXTTEXTOUTA
---

# EMREXTTEXTOUTA structure


## -description

The <b>EMREXTTEXTOUTA</b> and <b>EMREXTTEXTOUTW</b> structures contain members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>, or <a href="/windows/desktop/api/winuser/nf-winuser-drawtext">DrawText</a> enhanced metafile records.

## -struct-fields

### -field emr

Base structure for all record types.

### -field rclBounds

Bounding rectangle, in device units.

### -field iGraphicsMode

Current graphics mode. This member can be either the GM_COMPATIBLE or GM_ADVANCED value.

### -field exScale

X-scaling factor from page units to .01mm units if the graphics mode is the GM_COMPATIBLE value.

### -field eyScale

Y-scaling factor from page units to .01mm units if the graphics mode is the GM_COMPATIBLE value.

### -field emrtext

<b>EMRTEXT</b> structure, which is followed by the string and the intercharacter spacing array.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>