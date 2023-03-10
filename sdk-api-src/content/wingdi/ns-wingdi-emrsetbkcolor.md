---
UID: NS:wingdi.tagEMRSETTEXTCOLOR
title: EMRSETBKCOLOR (wingdi.h)
description: The EMRSETBKCOLOR and EMRSETTEXTCOLOR structures contain members for the SetBkColor and SetTextColor enhanced metafile records.
helpviewer_keywords: ["*PEMRSETBKCOLOR","*PEMRSETTEXTCOLOR","EMRSETBKCOLOR","EMRSETBKCOLOR structure [Windows GDI]","EMRSETBKCOLOR","EMRSETTEXTCOLOR","EMRSETBKCOLOR","EMRSETTEXTCOLOR structure [Windows GDI]","EMRSETTEXTCOLOR","EMRSETTEXTCOLOR structure [Windows GDI]","PEMRSETBKCOLOR","PEMRSETBKCOLOR structure pointer [Windows GDI]","PEMRSETTEXTCOLOR","PEMRSETTEXTCOLOR structure pointer [Windows GDI]","_win32_EMRSETBKCOLOR_str","gdi.emrsetbkcolor__emrsettextcolor","wingdi/EMRSETBKCOLOR","EMRSETTEXTCOLOR","wingdi/EMRSETTEXTCOLOR","wingdi/PEMRSETBKCOLOR","wingdi/PEMRSETTEXTCOLOR"]
old-location: gdi\emrsetbkcolor__emrsettextcolor.htm
tech.root: gdi
ms.assetid: 9916fc79-cac0-4c46-8fa5-aeca3b7f2cf0
ms.date: 12/05/2018
ms.keywords: '*PEMRSETBKCOLOR, *PEMRSETTEXTCOLOR, EMRSETBKCOLOR, EMRSETBKCOLOR structure [Windows GDI], EMRSETBKCOLOR,EMRSETTEXTCOLOR, EMRSETBKCOLOR,EMRSETTEXTCOLOR structure [Windows GDI], EMRSETTEXTCOLOR, EMRSETTEXTCOLOR structure [Windows GDI], PEMRSETBKCOLOR, PEMRSETBKCOLOR structure pointer [Windows GDI], PEMRSETTEXTCOLOR, PEMRSETTEXTCOLOR structure pointer [Windows GDI], _win32_EMRSETBKCOLOR_str, gdi.emrsetbkcolor__emrsettextcolor, wingdi/EMRSETBKCOLOR,EMRSETTEXTCOLOR, wingdi/EMRSETTEXTCOLOR, wingdi/PEMRSETBKCOLOR, wingdi/PEMRSETTEXTCOLOR'
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
req.typenames: EMRSETBKCOLOR, *PEMRSETBKCOLOR, EMRSETTEXTCOLOR, *PEMRSETTEXTCOLOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSETTEXTCOLOR
 - wingdi/tagEMRSETTEXTCOLOR
 - PEMRSETBKCOLOR
 - wingdi/PEMRSETBKCOLOR
 - EMRSETBKCOLOR
 - wingdi/EMRSETBKCOLOR
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
 - EMRSETBKCOLOR
---

# EMRSETBKCOLOR structure


## -description

The <b>EMRSETBKCOLOR</b> and <b>EMRSETTEXTCOLOR</b> structures contain members for the <b>SetBkColor</b> and <b>SetTextColor</b> enhanced metafile records.

## -struct-fields

### -field emr

Base structure for all record types.

### -field crColor

Color value. To make a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>