---
UID: NS:textstor.TS_SELECTION_ANCHOR
title: TS_SELECTION_ANCHOR (textstor.h)
description: The TS_SELECTION_ANCHOR structure contains anchor-based text selection data.
helpviewer_keywords: ["TS_SELECTION_ANCHOR","TS_SELECTION_ANCHOR structure [Text Services Framework]","_tsf_ts_selection_anchor_ref","textstor/TS_SELECTION_ANCHOR","tsf.ts_selection_anchor"]
old-location: tsf\ts_selection_anchor.htm
tech.root: TSF
ms.assetid: 56fbe145-1972-4b44-a730-17860e428dd0
ms.date: 12/05/2018
ms.keywords: TS_SELECTION_ANCHOR, TS_SELECTION_ANCHOR structure [Text Services Framework], _tsf_ts_selection_anchor_ref, textstor/TS_SELECTION_ANCHOR, tsf.ts_selection_anchor
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
req.typenames: TS_SELECTION_ANCHOR
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TS_SELECTION_ANCHOR
 - textstor/TS_SELECTION_ANCHOR
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
 - TS_SELECTION_ANCHOR
---

# TS_SELECTION_ANCHOR structure


## -description

The <b>TS_SELECTION_ANCHOR</b> structure contains anchor-based text selection data.

## -struct-fields

### -field paStart

Contains the start anchor of the selection.

### -field paEnd

Contains the end anchor of the selection.

### -field style

A <a href="/windows/desktop/api/textstor/ns-textstor-ts_selectionstyle">TS_SELECTIONSTYLE</a> structure that contains additional selection data.

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getselection">ITextStoreAnchor::GetSelection
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-setselection">ITextStoreAnchor::SetSelection
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_selectionstyle">TS_SELECTIONSTYLE
      </a>