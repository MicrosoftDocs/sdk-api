---
UID: NS:winuser.tagDRAWTEXTPARAMS
title: DRAWTEXTPARAMS (winuser.h)
description: The DRAWTEXTPARAMS structure contains extended formatting options for the DrawTextEx function.
helpviewer_keywords: ["*LPDRAWTEXTPARAMS","DRAWTEXTPARAMS","DRAWTEXTPARAMS structure [Windows GDI]","LPDRAWTEXTPARAMS","LPDRAWTEXTPARAMS structure pointer [Windows GDI]","_win32_DRAWTEXTPARAMS_str","gdi.drawtextparams","tagDRAWTEXTPARAMS","winuser/DRAWTEXTPARAMS","winuser/LPDRAWTEXTPARAMS"]
old-location: gdi\drawtextparams.htm
tech.root: gdi
ms.assetid: d3b89ce2-9a05-42af-b03e-24e1c4d6ef1d
ms.date: 12/05/2018
ms.keywords: '*LPDRAWTEXTPARAMS, DRAWTEXTPARAMS, DRAWTEXTPARAMS structure [Windows GDI], LPDRAWTEXTPARAMS, LPDRAWTEXTPARAMS structure pointer [Windows GDI], _win32_DRAWTEXTPARAMS_str, gdi.drawtextparams, tagDRAWTEXTPARAMS, winuser/DRAWTEXTPARAMS, winuser/LPDRAWTEXTPARAMS'
req.header: winuser.h
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
req.typenames: DRAWTEXTPARAMS, *LPDRAWTEXTPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDRAWTEXTPARAMS
 - winuser/tagDRAWTEXTPARAMS
 - LPDRAWTEXTPARAMS
 - winuser/LPDRAWTEXTPARAMS
 - DRAWTEXTPARAMS
 - winuser/DRAWTEXTPARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - DRAWTEXTPARAMS
---

# DRAWTEXTPARAMS structure


## -description

The <b>DRAWTEXTPARAMS</b> structure contains extended formatting options for the <a href="/windows/desktop/api/winuser/nf-winuser-drawtextexa">DrawTextEx</a> function.

## -struct-fields

### -field cbSize

The structure size, in bytes.

### -field iTabLength

The size of each tab stop, in units equal to the average character width.

### -field iLeftMargin

The left margin, in units equal to the average character width.

### -field iRightMargin

The right margin, in units equal to the average character width.

### -field uiLengthDrawn

Receives the number of characters processed by <a href="/windows/desktop/api/winuser/nf-winuser-drawtextexa">DrawTextEx</a>, including white-space characters. The number can be the <a href="/windows/desktop/gdi/specifying-length-of-text-output-string">length of the string</a> or the index of the first line that falls below the drawing area. Note that <b>DrawTextEx</b> always processes the entire string if the DT_NOCLIP formatting flag is specified.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-drawtextexa">DrawTextEx</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>