---
UID: NS:commctrl._HD_TEXTFILTERA
title: HD_TEXTFILTERA (commctrl.h)
description: Contains information about header control text filters. (ANSI)
helpviewer_keywords: ["*LPHD_TEXTFILTERA","HDTEXTFILTER","HDTEXTFILTER structure [Windows Controls]","HD_TEXTFILTERA","HD_TEXTFILTERW","LPHD_TEXTFILTER","LPHD_TEXTFILTER structure pointer [Windows Controls]","_HD_TEXTFILTERA","_HD_TEXTFILTERW","_win32_HDTEXTFILTER_Structure","_win32_HDTEXTFILTER_Structure_cpp","commctrl/HDTEXTFILTER","commctrl/LPHD_TEXTFILTER","controls.HDTEXTFILTER","controls._win32_HDTEXTFILTER_Structure"]
old-location: controls\HDTEXTFILTER.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\structures\hdtextfilter.htm
ms.date: 12/05/2018
ms.keywords: '*LPHD_TEXTFILTERA, HDTEXTFILTER, HDTEXTFILTER structure [Windows Controls], HD_TEXTFILTERA, HD_TEXTFILTERW, LPHD_TEXTFILTER, LPHD_TEXTFILTER structure pointer [Windows Controls], _HD_TEXTFILTERA, _HD_TEXTFILTERW, _win32_HDTEXTFILTER_Structure, _win32_HDTEXTFILTER_Structure_cpp, commctrl/HDTEXTFILTER, commctrl/LPHD_TEXTFILTER, controls.HDTEXTFILTER, controls._win32_HDTEXTFILTER_Structure'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: HD_TEXTFILTERA, *LPHD_TEXTFILTERA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HD_TEXTFILTERA
 - commctrl/_HD_TEXTFILTERA
 - LPHD_TEXTFILTERA
 - commctrl/LPHD_TEXTFILTERA
 - HD_TEXTFILTERA
 - commctrl/HD_TEXTFILTERA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - HDTEXTFILTER
 - HD_TEXTFILTERA
 - HD_TEXTFILTERW
---

# HD_TEXTFILTERA structure


## -description

Contains information about header control text filters.

## -struct-fields

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to the buffer containing the filter.

### -field cchTextMax

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

A value specifying the maximum size, in characters, for an edit control buffer.

## -remarks

> [!NOTE]
> The commctrl.h header defines HD_TEXTFILTER as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
