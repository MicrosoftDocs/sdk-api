---
UID: NS:sbe.__MIDL___MIDL_itf_sbe_0000_0015_0002
title: DVR_STREAM_DESC (sbe.h)
description: Describes a stream captured by a tuner.
helpviewer_keywords: ["DVR_STREAM_DESC","DVR_STREAM_DESC structure [Microsoft TV Technologies]","PDVR_STREAM_DESC","PDVR_STREAM_DESC structure pointer [Microsoft TV Technologies]","mstv.dvr_stream_desc","sbe/DVR_STREAM_DESC","sbe/PDVR_STREAM_DESC"]
old-location: mstv\dvr_stream_desc.htm
tech.root: mstv
ms.assetid: 1c4ac3bc-3d0c-4f06-a146-2e39439ebb05
ms.date: 12/05/2018
ms.keywords: DVR_STREAM_DESC, DVR_STREAM_DESC structure [Microsoft TV Technologies], PDVR_STREAM_DESC, PDVR_STREAM_DESC structure pointer [Microsoft TV Technologies], mstv.dvr_stream_desc, sbe/DVR_STREAM_DESC, sbe/PDVR_STREAM_DESC
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DVR_STREAM_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_sbe_0000_0015_0002
 - sbe/__MIDL___MIDL_itf_sbe_0000_0015_0002
 - DVR_STREAM_DESC
 - sbe/DVR_STREAM_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - sbe.h
api_name:
 - DVR_STREAM_DESC
---

# DVR_STREAM_DESC structure


## -description

Describes a stream captured by a tuner.

## -struct-fields

### -field Version

### -field StreamId

Specifies a unique identifier for the stream.

### -field Default

Indicates whether or not the stream is the default stream.

### -field Creation

Indicates whether or not the stream has been created.

### -field Reserved

Reserved.

### -field guidSubMediaType

Specifies the GUID corresponding to the media subtype.

### -field guidFormatType

Specifies the GUID corresponding to the major media type of the stream.

### -field MediaType

Defines the major media type of the stream.

### -field version

Specifies the stream's version number.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-structures">Stream Buffer Engine Structures</a>