---
UID: NS:wmsdkidl._WMLeakyBucketPair
title: WM_LEAKY_BUCKET_PAIR (wmsdkidl.h)
description: The WM_LEAKY_BUCKET_PAIR structure describes the buffering requirements for a VBR file. This structure is used with the ASFLeakyBucketPairs attribute.
helpviewer_keywords: ["WM_LEAKY_BUCKET_PAIR","WM_LEAKY_BUCKET_PAIR structure [windows Media Format]","wmformat.wm_leaky_bucket_pair","wmsdkidl/WM_LEAKY_BUCKET_PAIR"]
old-location: wmformat\wm_leaky_bucket_pair.htm
tech.root: wmformat
ms.assetid: 8fada83d-cb66-4411-9ff5-0eb4c02a3b5f
ms.date: 4/26/2023
ms.keywords: WM_LEAKY_BUCKET_PAIR, WM_LEAKY_BUCKET_PAIR structure [windows Media Format], wmformat.wm_leaky_bucket_pair, wmsdkidl/WM_LEAKY_BUCKET_PAIR
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
req.typenames: WM_LEAKY_BUCKET_PAIR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMLeakyBucketPair
 - wmsdkidl/_WMLeakyBucketPair
 - WM_LEAKY_BUCKET_PAIR
 - wmsdkidl/WM_LEAKY_BUCKET_PAIR
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
 - WM_LEAKY_BUCKET_PAIR
---

# WM_LEAKY_BUCKET_PAIR structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WM_LEAKY_BUCKET_PAIR</b> structure describes the buffering requirements for a VBR file. This structure is used with the <a href="/windows/desktop/wmformat/asfleakybucketpairs">ASFLeakyBucketPairs</a> attribute.

## -struct-fields

### -field dwBitrate

Bit rate, in bits per second.

### -field msBufferWindow

Size of the buffer window, in milliseconds.

## -remarks

The <b>ASFLeakyBucketPairs</b> attribute gives a list of bit rates and corresponding buffer windows. For each bit rate, the <b>msBufferWindow</b> member indicates how much content the reader object will buffer before it begins playback. The size of the buffer in bytes equals <b>msBufferWindow</b> x <b>dwBitrate</b> / 8000.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>
