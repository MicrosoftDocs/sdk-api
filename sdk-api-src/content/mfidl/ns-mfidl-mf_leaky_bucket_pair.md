---
UID: NS:mfidl._MF_LEAKY_BUCKET_PAIR
title: MF_LEAKY_BUCKET_PAIR (mfidl.h)
description: Specifies the buffering requirements of a file.
helpviewer_keywords: ["MF_LEAKY_BUCKET_PAIR","MF_LEAKY_BUCKET_PAIR structure [Media Foundation]","aa95a8f0-2f4c-4d7e-81c3-8a14a6ffa54e","mf.mf_leaky_bucket_pair","mfidl/MF_LEAKY_BUCKET_PAIR"]
old-location: mf\mf_leaky_bucket_pair.htm
tech.root: mf
ms.assetid: aa95a8f0-2f4c-4d7e-81c3-8a14a6ffa54e
ms.date: 12/05/2018
ms.keywords: MF_LEAKY_BUCKET_PAIR, MF_LEAKY_BUCKET_PAIR structure [Media Foundation], aa95a8f0-2f4c-4d7e-81c3-8a14a6ffa54e, mf.mf_leaky_bucket_pair, mfidl/MF_LEAKY_BUCKET_PAIR
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MF_LEAKY_BUCKET_PAIR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_LEAKY_BUCKET_PAIR
 - mfidl/_MF_LEAKY_BUCKET_PAIR
 - MF_LEAKY_BUCKET_PAIR
 - mfidl/MF_LEAKY_BUCKET_PAIR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_LEAKY_BUCKET_PAIR
---

# MF_LEAKY_BUCKET_PAIR structure


## -description

Specifies the buffering requirements of a file.

## -struct-fields

### -field dwBitrate

Bit rate, in bits per second.

### -field msBufferWindow

Size of the buffer window, in milliseconds.

## -remarks

This structure describes the buffering requirements for content encoded at the bit rate specified in the <b>dwBitrate</b>. The <b>msBufferWindow</b> member indicates how much data should be buffered before starting playback. The size of the buffer in bytes is <b>msBufferWinow</b>×<b>dwBitrate</b> / 8000.

## -see-also

<a href="/windows/desktop/api/mfidl/ns-mfidl-mfbytestream_buffering_params">MFBYTESTREAM_BUFFERING_PARAMS</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>