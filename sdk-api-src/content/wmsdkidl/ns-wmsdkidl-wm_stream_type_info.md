---
UID: NS:wmsdkidl._WMStreamTypeInfo
title: WM_STREAM_TYPE_INFO (wmsdkidl.h)
description: The WM_STREAM_TYPE_INFO structure is used as the data item for the WM/StreamTypeInfo complex metadata attribute. It stores the major type and the size of the associated format data.
helpviewer_keywords: ["WM_STREAM_TYPE_INFO","WM_STREAM_TYPE_INFO structure [windows Media Format]","structure [windows Media Format]","wmformat.wm_stream_type_info","wmsdkidl/WM_STREAM_TYPE_INFO"]
old-location: wmformat\wm_stream_type_info.htm
tech.root: wmformat
ms.assetid: 9e8f2670-555a-478a-99c2-3a4de7f8cfa1
ms.date: 4/26/2023
ms.keywords: WM_STREAM_TYPE_INFO, WM_STREAM_TYPE_INFO structure [windows Media Format], structure [windows Media Format], wmformat.wm_stream_type_info, wmsdkidl/WM_STREAM_TYPE_INFO
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
req.typenames: WM_STREAM_TYPE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMStreamTypeInfo
 - wmsdkidl/_WMStreamTypeInfo
 - WM_STREAM_TYPE_INFO
 - wmsdkidl/WM_STREAM_TYPE_INFO
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
 - WM_STREAM_TYPE_INFO
---

# WM_STREAM_TYPE_INFO structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WM_STREAM_TYPE_INFO</b> structure is used as the data item for the <a href="/windows/desktop/wmformat/wm-streamtypeinfo">WM/StreamTypeInfo</a> complex metadata attribute. It stores the major type and the size of the associated format data.

## -struct-fields

### -field guidMajorType

The major type of the stream.

### -field cbFormat

The size of format in bytes.

## -remarks

None.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>