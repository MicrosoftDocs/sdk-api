---
UID: NS:wingdi.tagAXESLISTA
title: AXESLISTA (wingdi.h)
description: The AXESLIST structure contains information on all the axes of a multiple master font. (ANSI)
helpviewer_keywords: ["*LPAXESLISTA","*PAXESLISTA","AXESLIST","AXESLIST structure [Windows GDI]","AXESLISTA","AXESLISTW","PAXESLIST","PAXESLIST structure pointer [Windows GDI]","_win32_AXESLIST_str","gdi.axeslist","wingdi/AXESLIST","wingdi/AXESLISTA","wingdi/AXESLISTW","wingdi/PAXESLIST"]
old-location: gdi\axeslist.htm
tech.root: gdi
ms.assetid: f95f012e-f02b-46c1-94ba-69f426ee7ad9
ms.date: 12/05/2018
ms.keywords: '*LPAXESLISTA, *PAXESLISTA, AXESLIST, AXESLIST structure [Windows GDI], AXESLISTA, AXESLISTW, PAXESLIST, PAXESLIST structure pointer [Windows GDI], _win32_AXESLIST_str, gdi.axeslist, wingdi/AXESLIST, wingdi/AXESLISTA, wingdi/AXESLISTW, wingdi/PAXESLIST'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AXESLISTW (Unicode) and AXESLISTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AXESLISTA, *PAXESLISTA, *LPAXESLISTA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAXESLISTA
 - wingdi/tagAXESLISTA
 - PAXESLISTA
 - wingdi/PAXESLISTA
 - AXESLISTA
 - wingdi/AXESLISTA
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
 - AXESLIST
 - AXESLISTA
 - AXESLISTW
---

# AXESLISTA structure


## -description

The <b>AXESLIST</b> structure contains information on all the axes of a multiple master font.

## -struct-fields

### -field axlReserved

Reserved. Must be STAMP_AXESLIST.

### -field axlNumAxes

Number of axes for a specified multiple master font.

### -field axlAxisInfo

An array of <a href="/windows/desktop/api/wingdi/ns-wingdi-axisinfoa">AXISINFO</a> structures. Each <b>AXISINFO</b> structure contains information on an axis of a specified multiple master font. This corresponds to the <b>dvValues</b> array in the <a href="/windows/desktop/api/wingdi/ns-wingdi-designvector">DESIGNVECTOR</a> structure.

## -remarks

The PostScript Open Type Font does not support multiple master functionality.

The information on the axes of a multiple master font are specified by the <a href="/windows/desktop/api/wingdi/ns-wingdi-axisinfoa">AXISINFO</a> structures. The <b>axlNumAxes</b> member specifies the actual size of <b>axlAxisInfo</b>, while MM_MAX_NUMAXES, which equals 16, is the maximum allowed size of <b>axlAxisInfo</b>.





> [!NOTE]
> The wingdi.h header defines AXESLIST as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-axisinfoa">AXISINFO</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-designvector">DESIGNVECTOR</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-enumtextmetrica">ENUMTEXTMETRIC</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>
