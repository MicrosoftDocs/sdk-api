---
UID: NS:wmsdkidl._WMT_BUFFER_SEGMENT
title: WMT_BUFFER_SEGMENT (wmsdkidl.h)
description: The WMT_BUFFER_SEGMENT structure contains the information needed to specify a segment in a buffer. It is used as a member of the WMT_FILESINK_DATA_UNIT and WMT_PAYLOAD_FRAGMENT structures to specify segments of a packet.
helpviewer_keywords: ["WMT_BUFFER_SEGMENT","WMT_BUFFER_SEGMENT structure [windows Media Format]","wmformat.wmt_buffer_segment","wmsdkidl/WMT_BUFFER_SEGMENT"]
old-location: wmformat\wmt_buffer_segment.htm
tech.root: wmformat
ms.assetid: 047e19da-c819-46e5-8a1c-09bc93a05259
ms.date: 12/05/2018
ms.keywords: WMT_BUFFER_SEGMENT, WMT_BUFFER_SEGMENT structure [windows Media Format], wmformat.wmt_buffer_segment, wmsdkidl/WMT_BUFFER_SEGMENT
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
req.typenames: WMT_BUFFER_SEGMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMT_BUFFER_SEGMENT
 - wmsdkidl/_WMT_BUFFER_SEGMENT
 - WMT_BUFFER_SEGMENT
 - wmsdkidl/WMT_BUFFER_SEGMENT
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
 - WMT_BUFFER_SEGMENT
---

# WMT_BUFFER_SEGMENT structure


## -description

The <b>WMT_BUFFER_SEGMENT</b> structure contains the information needed to specify a segment in a buffer. It is used as a member of the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit">WMT_FILESINK_DATA_UNIT</a> and <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_payload_fragment">WMT_PAYLOAD_FRAGMENT</a> structures to specify segments of a packet.

## -struct-fields

### -field pBuffer

Pointer to a buffer object containing the buffer segment.

### -field cbOffset

The offset, in bytes, from the start of the buffer to the buffer segment.

### -field cbLength

The length, in bytes, of the buffer segment.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>