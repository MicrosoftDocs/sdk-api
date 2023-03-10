---
UID: NS:textstor.TS_SELECTIONSTYLE
title: TS_SELECTIONSTYLE (textstor.h)
description: The TS_SELECTIONSTYLE structure represents the style of a selection.
helpviewer_keywords: ["TS_SELECTIONSTYLE","TS_SELECTIONSTYLE structure [Text Services Framework]","_tsf_ts_selectionstyle_ref","textstor/TS_SELECTIONSTYLE","tsf.ts_selectionstyle"]
old-location: tsf\ts_selectionstyle.htm
tech.root: TSF
ms.assetid: 20d0efc2-604f-4ec6-820d-0f87a6d011b0
ms.date: 12/05/2018
ms.keywords: TS_SELECTIONSTYLE, TS_SELECTIONSTYLE structure [Text Services Framework], _tsf_ts_selectionstyle_ref, textstor/TS_SELECTIONSTYLE, tsf.ts_selectionstyle
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TS_SELECTIONSTYLE
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TS_SELECTIONSTYLE
 - textstor/TS_SELECTIONSTYLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Textstor.h
api_name:
 - TS_SELECTIONSTYLE
---

# TS_SELECTIONSTYLE structure


## -description

The <b>TS_SELECTIONSTYLE</b> structure represents the style of a selection.

## -struct-fields

### -field ase

Specifies the active end of the selection. For more information, see <a href="/windows/win32/api/textstor/ne-textstor-tsactiveselend">TsActiveSelEnd</a>.

### -field fInterimChar

Indicates if the selection is an interim character. If this value is nonzero, then the selection is an interim character and <b>ase</b> will be TS_AE_NONE. If this value is zero, the selection is not an interim character.

## -remarks

An interim character selection is the length of one character and is visually represented as a solid rectangle that is usually flashing. This is a standard UI element of Korean and some Chinese character compositions. <b>fInterimChar</b> is an indication that a specific character is being composed. <b>fInterimChar</b> can only be nonzero for a single selection. In this case, there will be no caret because the highlight takes its place.

## -see-also

<a href="/windows/desktop/api/textstor/ns-textstor-ts_selection_acp">TS_SELECTION_ACP
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_selection_anchor">TS_SELECTION_ANCHOR
      </a>



<a href="/windows/win32/api/textstor/ne-textstor-tsactiveselend">TsActiveSelEnd
      </a>