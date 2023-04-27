---
UID: NE:wmsdkidl.tagWMT_INDEXER_TYPE
title: WMT_INDEXER_TYPE (wmsdkidl.h)
description: The WMT_INDEXER_TYPE enumeration type defines the types of indexing supported by the indexer.
helpviewer_keywords: ["WMT_INDEXER_TYPE","WMT_INDEXER_TYPE enumeration [windows Media Format]","WMT_IT_FRAME_NUMBERS","WMT_IT_PRESENTATION_TIME","WMT_IT_TIMECODE","wmformat.wmt_indexer_type","wmsdkidl/WMT_INDEXER_TYPE","wmsdkidl/WMT_IT_FRAME_NUMBERS","wmsdkidl/WMT_IT_PRESENTATION_TIME","wmsdkidl/WMT_IT_TIMECODE"]
old-location: wmformat\wmt_indexer_type.htm
tech.root: wmformat
ms.assetid: 1b80511c-175f-4d05-8ce6-d048a9e77223
ms.date: 12/05/2018
ms.keywords: WMT_INDEXER_TYPE, WMT_INDEXER_TYPE enumeration [windows Media Format], WMT_IT_FRAME_NUMBERS, WMT_IT_PRESENTATION_TIME, WMT_IT_TIMECODE, wmformat.wmt_indexer_type, wmsdkidl/WMT_INDEXER_TYPE, wmsdkidl/WMT_IT_FRAME_NUMBERS, wmsdkidl/WMT_IT_PRESENTATION_TIME, wmsdkidl/WMT_IT_TIMECODE
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.typenames: WMT_INDEXER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWMT_INDEXER_TYPE
 - wmsdkidl/tagWMT_INDEXER_TYPE
 - WMT_INDEXER_TYPE
 - wmsdkidl/WMT_INDEXER_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_INDEXER_TYPE
---

# WMT_INDEXER_TYPE enumeration


## -description

The <b>WMT_INDEXER_TYPE</b> enumeration type defines the types of indexing supported by the indexer.

## -enum-fields

### -field WMT_IT_PRESENTATION_TIME:0

The indexer will construct an index using presentation times as indexes.

### -field WMT_IT_FRAME_NUMBERS

The indexer will construct an index using frame numbers as indexes.

### -field WMT_IT_TIMECODE

The indexer will construct an index using SMPTE time codes as indexes.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
