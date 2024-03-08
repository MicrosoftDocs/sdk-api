---
UID: NS:wmsdkidl._WMT_WEBSTREAM_SAMPLE_HEADER
title: WMT_WEBSTREAM_SAMPLE_HEADER (wmsdkidl.h)
description: The WMT_WEBSTREAM_SAMPLE_HEADER structure is used as a variable-sized header for each Web stream sample.
helpviewer_keywords: ["WMT_WEBSTREAM_SAMPLE_HEADER","WMT_WEBSTREAM_SAMPLE_HEADER structure [windows Media Format]","wmformat.wmt_webstream_sample_header","wmsdkidl/WMT_WEBSTREAM_SAMPLE_HEADER"]
old-location: wmformat\wmt_webstream_sample_header.htm
tech.root: wmformat
ms.assetid: 5492af92-4829-4bf1-8512-3d57fbe70ce5
ms.date: 4/26/2023
ms.keywords: WMT_WEBSTREAM_SAMPLE_HEADER, WMT_WEBSTREAM_SAMPLE_HEADER structure [windows Media Format], wmformat.wmt_webstream_sample_header, wmsdkidl/WMT_WEBSTREAM_SAMPLE_HEADER
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
req.typenames: WMT_WEBSTREAM_SAMPLE_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMT_WEBSTREAM_SAMPLE_HEADER
 - wmsdkidl/_WMT_WEBSTREAM_SAMPLE_HEADER
 - WMT_WEBSTREAM_SAMPLE_HEADER
 - wmsdkidl/WMT_WEBSTREAM_SAMPLE_HEADER
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
 - WMT_WEBSTREAM_SAMPLE_HEADER
---

# WMT_WEBSTREAM_SAMPLE_HEADER structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMT_WEBSTREAM_SAMPLE_HEADER</b> structure is used as a variable-sized header for each Web stream sample.

## -struct-fields

### -field cbLength

<b>WORD</b> containing the size of <b>wszURL</b> in wide characters.

### -field wPart

<b>WORD</b> containing the zero-based part number to which the sample applies. When the last part is received, <b>wPart</b> equals <b>cTotalParts</b>– 1.

### -field cTotalParts

<b>WORD</b> containing the total number of parts in the Web stream.

### -field wSampleType

<b>WORD</b> containing the type of Web stream, either WEBSTREAM_SAMPLE_TYPE_FILE (0x1) or WEBSTREAM_SAMPLE_TYPE_RENDER (0x2). See Remarks.

### -field wszURL

Wide-character null-terminated string specifying the local URL.

## -remarks

In a Web stream, each sample begins with this structure. The application is responsible for determining the size of the structure for each sample delivered. The size depends on the length of the <b>wszURL</b> member, as reported in the <b>cbLength</b> member.

If <b>wSampleType</b> is WEBSTREAM_SAMPLE_TYPE_FILE, the sample contains data immediately following the header that should be cached for later rendering. If the type is WEBSTREAM_SAMPLE_TYPE_RENDER, the sample contains no data. The application should cause the file named in the <b>wszURL</b> member to be immediately rendered on the display.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>