---
UID: NS:textstor.TS_SELECTION_ACP
title: TS_SELECTION_ACP (textstor.h)
description: The TS_SELECTION_ACP structure contains ACP-based text selection data.
helpviewer_keywords: ["TS_SELECTION_ACP","TS_SELECTION_ACP structure [Text Services Framework]","_tsf_ts_selection_acp_ref","textstor/TS_SELECTION_ACP","tsf.ts_selection_acp"]
old-location: tsf\ts_selection_acp.htm
tech.root: TSF
ms.assetid: 739c87c5-3e9c-41f3-ad79-0b417347604b
ms.date: 12/05/2018
ms.keywords: TS_SELECTION_ACP, TS_SELECTION_ACP structure [Text Services Framework], _tsf_ts_selection_acp_ref, textstor/TS_SELECTION_ACP, tsf.ts_selection_acp
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
req.typenames: TS_SELECTION_ACP
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TS_SELECTION_ACP
 - textstor/TS_SELECTION_ACP
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
 - TS_SELECTION_ACP
---

# TS_SELECTION_ACP structure


## -description

The <b>TS_SELECTION_ACP</b> structure contains ACP-based text selection data.

## -struct-fields

### -field acpStart

Contains the start position of the selection.

### -field acpEnd

Contains the end position of the selection.

### -field style

A <a href="/windows/desktop/api/textstor/ns-textstor-ts_selectionstyle">TS_SELECTIONSTYLE</a> structure that contains additional selection data.

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getselection">ITextStoreACP::GetSelection
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-setselection">ITextStoreACP::SetSelection
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_selectionstyle">TS_SELECTIONSTYLE
      </a>