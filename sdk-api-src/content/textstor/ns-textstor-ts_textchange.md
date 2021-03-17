---
UID: NS:textstor.TS_TEXTCHANGE
title: TS_TEXTCHANGE (textstor.h)
description: The TS_TEXTCHANGE structure contains text change data.
helpviewer_keywords: ["TS_TEXTCHANGE","TS_TEXTCHANGE structure [Text Services Framework]","_tsf_ts_textchange_ref","textstor/TS_TEXTCHANGE","tsf.ts_textchange"]
old-location: tsf\ts_textchange.htm
tech.root: TSF
ms.assetid: af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0
ms.date: 12/05/2018
ms.keywords: TS_TEXTCHANGE, TS_TEXTCHANGE structure [Text Services Framework], _tsf_ts_textchange_ref, textstor/TS_TEXTCHANGE, tsf.ts_textchange
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
req.typenames: TS_TEXTCHANGE
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TS_TEXTCHANGE
 - textstor/TS_TEXTCHANGE
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
 - TS_TEXTCHANGE
---

# TS_TEXTCHANGE structure


## -description

The <b>TS_TEXTCHANGE</b> structure contains text change data.

## -struct-fields

### -field acpStart

Contains the starting character position of the change.

### -field acpOldEnd

Contains the ending character position before the text is changed.

### -field acpNewEnd

Contains the ending character position after the text is changed.

## -remarks

The possible text changes include insert, delete, and replace. For example, if you replace the first "t" of "text" with "T", <b>acpStart</b> =0, <b>acpOldEnd</b> =1, and <b>acpNewEnd</b> =1. If you delete the last "t", <b>acpStart</b> =3, <b>acpOldEnd</b> =4, and <b>acpNewEnd</b> =3. If an "a" is inserted between "e" and "x", <b>acpStart</b> =2, <b>acpOldEnd</b> =2, and <b>acpNewEnd</b> =3.

