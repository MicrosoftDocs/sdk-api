---
UID: NE:textstor.__MIDL___MIDL_itf_textstor_0000_0000_0001
title: TsActiveSelEnd (textstor.h)
description: Elements of the TsActiveSelEnd enumeration specify which end of a text store selection is active.
helpviewer_keywords: ["TS_AE_END","TS_AE_NONE","TS_AE_START","TsActiveSelEnd","TsActiveSelEnd enumeration [Text Services Framework]","_tsf_tsactiveselend_ref","textstor/TS_AE_END","textstor/TS_AE_NONE","textstor/TS_AE_START","textstor/TsActiveSelEnd","tsf.tsactiveselend"]
old-location: tsf\tsactiveselend.htm
tech.root: TSF
ms.assetid: 95695f10-2296-41fe-b2b4-efae548292bb
ms.date: 12/05/2018
ms.keywords: TS_AE_END, TS_AE_NONE, TS_AE_START, TsActiveSelEnd, TsActiveSelEnd enumeration [Text Services Framework], _tsf_tsactiveselend_ref, textstor/TS_AE_END, textstor/TS_AE_NONE, textstor/TS_AE_START, textstor/TsActiveSelEnd, tsf.tsactiveselend
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
req.typenames: TsActiveSelEnd
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_textstor_0000_0000_0001
 - textstor/__MIDL___MIDL_itf_textstor_0000_0000_0001
 - TsActiveSelEnd
 - textstor/TsActiveSelEnd
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
 - TsActiveSelEnd
---

# TsActiveSelEnd enumeration


## -description

Elements of the <b>TsActiveSelEnd</b> enumeration specify which end of a text store selection is active.

## -enum-fields

### -field TS_AE_NONE:0

The selection has no active end. This is typical for all selections other than the default selection.

### -field TS_AE_START:1

The active end of the selection is at the start of the range of text.

### -field TS_AE_END:2

The active end of the selection is at the end of the range of text.

## -remarks

The active end of a selection is the end likely to respond to user actions. For example, in many applications, holding down the SHIFT key while using the arrow keys will change the selection. The end of the selection that moves is the active end of the selection.

This enumeration is used in the <a href="/windows/desktop/api/textstor/ns-textstor-ts_selectionstyle">TS_SELECTIONSTYLE</a> structure.

## -see-also

<a href="/windows/desktop/api/textstor/ns-textstor-ts_selectionstyle">TS_SELECTIONSTYLE
      </a>
