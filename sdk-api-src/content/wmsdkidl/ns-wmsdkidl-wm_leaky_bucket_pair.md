---
UID: NS:wmsdkidl._WMLeakyBucketPair
title: WM_LEAKY_BUCKET_PAIR (wmsdkidl.h)
description: The WM_LEAKY_BUCKET_PAIR structure describes the buffering requirements for a VBR file. This structure is used with the ASFLeakyBucketPairs attribute.
helpviewer_keywords: ["WM_LEAKY_BUCKET_PAIR","WM_LEAKY_BUCKET_PAIR structure [windows Media Format]","wmformat.wm_leaky_bucket_pair","wmsdkidl/WM_LEAKY_BUCKET_PAIR"]
old-location: wmformat\wm_leaky_bucket_pair.htm
tech.root: wmformat
ms.assetid: 8fada83d-cb66-4411-9ff5-0eb4c02a3b5f
ms.date: 12/05/2018
ms.keywords: WM_LEAKY_BUCKET_PAIR, WM_LEAKY_BUCKET_PAIR structure [windows Media Format], wmformat.wm_leaky_bucket_pair, wmsdkidl/WM_LEAKY_BUCKET_PAIR
f1_keywords:
- wmsdkidl/WM_LEAKY_BUCKET_PAIR
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wmsdkidl.h
api_name:
- WM_LEAKY_BUCKET_PAIR
targetos: Windows
req.typenames: WM_LEAKY_BUCKET_PAIR
req.redist: 
ms.custom: 19H1
---

# WM_LEAKY_BUCKET_PAIR structure


## -description



The <b>WM_LEAKY_BUCKET_PAIR </b>structure describes the buffering requirements for a VBR file. This structure is used with the <a href="https://docs.microsoft.com/windows/desktop/wmformat/asfleakybucketpairs">ASFLeakyBucketPairs</a> attribute.




## -struct-fields




### -field dwBitrate

Bit rate, in bits per second.


### -field msBufferWindow

Size of the buffer window, in milliseconds.


## -remarks



The <b>ASFLeakyBucketPairs</b> attribute gives a list of bit rates and corresponding buffer windows. For each bit rate, the <b>msBufferWindow</b> member indicates how much content the reader object will buffer before it begins playback. The size of the buffer in bytes equals <b>msBufferWinow</b> x <b>dwBitrate</b> / 8000.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/structures">Structures</a>
 

 

