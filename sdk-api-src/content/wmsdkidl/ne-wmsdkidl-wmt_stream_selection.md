---
UID: NE:wmsdkidl.WMT_STREAM_SELECTION
title: WMT_STREAM_SELECTION (wmsdkidl.h)
description: The WMT_STREAM_SELECTION enumeration type defines the playback status of a stream.
helpviewer_keywords: ["WMT_CLEANPOINT_ONLY","WMT_OFF","WMT_ON","WMT_STREAM_SELECTION","WMT_STREAM_SELECTION enumeration [windows Media Format]","wmformat.wmt_stream_selection","wmsdkidl/WMT_CLEANPOINT_ONLY","wmsdkidl/WMT_OFF","wmsdkidl/WMT_ON","wmsdkidl/WMT_STREAM_SELECTION"]
old-location: wmformat\wmt_stream_selection.htm
tech.root: wmformat
ms.assetid: 7191d608-1a25-48c0-858b-c5e93f9d8e6e
ms.date: 12/05/2018
ms.keywords: WMT_CLEANPOINT_ONLY, WMT_OFF, WMT_ON, WMT_STREAM_SELECTION, WMT_STREAM_SELECTION enumeration [windows Media Format], wmformat.wmt_stream_selection, wmsdkidl/WMT_CLEANPOINT_ONLY, wmsdkidl/WMT_OFF, wmsdkidl/WMT_ON, wmsdkidl/WMT_STREAM_SELECTION
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.typenames: WMT_STREAM_SELECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMT_STREAM_SELECTION
 - wmsdkidl/WMT_STREAM_SELECTION
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
 - WMT_STREAM_SELECTION
---

# WMT_STREAM_SELECTION enumeration


## -description

The <b>WMT_STREAM_SELECTION</b> enumeration type defines the playback status of a stream.

## -enum-fields

### -field WMT_OFF:0

No samples will be delivered for the stream.

### -field WMT_CLEANPOINT_ONLY:1

Only samples with <a href="/windows/desktop/wmformat/wmformat-glossary">cleanpoints</a> will be delivered for the stream.

### -field WMT_ON:2

All samples will be delivered for the stream.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
