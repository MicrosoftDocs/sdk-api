---
UID: NE:mfobjects._MFBYTESTREAM_SEEK_ORIGIN
title: MFBYTESTREAM_SEEK_ORIGIN (mfobjects.h)
description: Specifies the origin for a seek request.
helpviewer_keywords: ["MFBYTESTREAM_SEEK_ORIGIN","MFBYTESTREAM_SEEK_ORIGIN enumeration [Media Foundation]","_MFBYTESTREAM_SEEK_ORIGIN","ad7ad61a-0c02-4a8f-96c3-33f7d1f0ce51","mf.mfbytestream_seek_origin","mfobjects/MFBYTESTREAM_SEEK_ORIGIN","mfobjects/msoBegin","mfobjects/msoCurrent","msoBegin","msoCurrent"]
old-location: mf\mfbytestream_seek_origin.htm
tech.root: mf
ms.assetid: ad7ad61a-0c02-4a8f-96c3-33f7d1f0ce51
ms.date: 12/05/2018
ms.keywords: MFBYTESTREAM_SEEK_ORIGIN, MFBYTESTREAM_SEEK_ORIGIN enumeration [Media Foundation], _MFBYTESTREAM_SEEK_ORIGIN, ad7ad61a-0c02-4a8f-96c3-33f7d1f0ce51, mf.mfbytestream_seek_origin, mfobjects/MFBYTESTREAM_SEEK_ORIGIN, mfobjects/msoBegin, mfobjects/msoCurrent, msoBegin, msoCurrent
req.header: mfobjects.h
req.include-header: Mfidl.h
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
req.typenames: MFBYTESTREAM_SEEK_ORIGIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFBYTESTREAM_SEEK_ORIGIN
 - mfobjects/_MFBYTESTREAM_SEEK_ORIGIN
 - MFBYTESTREAM_SEEK_ORIGIN
 - mfobjects/MFBYTESTREAM_SEEK_ORIGIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MFBYTESTREAM_SEEK_ORIGIN
---

# MFBYTESTREAM_SEEK_ORIGIN enumeration


## -description

Specifies the origin for a seek request.

## -enum-fields

### -field msoBegin:0

The seek position is specified relative to the start of the stream.

### -field msoCurrent

The seek position is specified relative to the current read/write position in the stream.

## -see-also

<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-seek">IMFByteStream::Seek</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
