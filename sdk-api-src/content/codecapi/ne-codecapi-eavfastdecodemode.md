---
UID: NE:codecapi.eAVFastDecodeMode
title: eAVFastDecodeMode (codecapi.h)
description: Specifies the video decoding speed. This enumeration is used with the AVDecVideoFastDecodeMode property.
helpviewer_keywords: ["codecapi/eAVFastDecodeMode","codecapi/eVideoDecodeCompliant","codecapi/eVideoDecodeDisableLF","codecapi/eVideoDecodeFastest","codecapi/eVideoDecodeOptimalLF","dshow.eavfastdecodemode","eAVFastDecodeMode","eAVFastDecodeMode enumeration [DirectShow]","eVideoDecodeCompliant","eVideoDecodeDisableLF","eVideoDecodeFastest","eVideoDecodeOptimalLF"]
old-location: dshow\eavfastdecodemode.htm
tech.root: dshow
ms.assetid: 526A52A8-4B48-43AE-A8B2-EE800C6BAE8F
ms.date: 12/05/2018
ms.keywords: codecapi/eAVFastDecodeMode, codecapi/eVideoDecodeCompliant, codecapi/eVideoDecodeDisableLF, codecapi/eVideoDecodeFastest, codecapi/eVideoDecodeOptimalLF, dshow.eavfastdecodemode, eAVFastDecodeMode, eAVFastDecodeMode enumeration [DirectShow], eVideoDecodeCompliant, eVideoDecodeDisableLF, eVideoDecodeFastest, eVideoDecodeOptimalLF
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eAVFastDecodeMode
 - codecapi/eAVFastDecodeMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVFastDecodeMode
---

# eAVFastDecodeMode enumeration


## -description

Specifies the video decoding speed. This enumeration is used with the <a href="/windows/desktop/DirectShow/avdecvideofastdecodemode">AVDecVideoFastDecodeMode</a> property.

## -enum-fields

### -field eVideoDecodeCompliant:0

Use normal decoding.

### -field eVideoDecodeOptimalLF:1

Use the optimal loop filter.

### -field eVideoDecodeDisableLF:2

Disable the loop filter.

### -field eVideoDecodeFastest:32

Use the fastest decoding mode.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
