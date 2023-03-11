---
UID: NE:mmstream.__MIDL___MIDL_itf_mmstream_0000_0000_0002
title: STREAM_STATE (mmstream.h)
description: Note  This API is deprecated. New applications should not use it. Describes the state of the stream.
helpviewer_keywords: ["STREAMSTATE_RUN","STREAMSTATE_STOP","STREAM_STATE","STREAM_STATE enumeration [DirectShow]","dshow.stream_state","mmstream/STREAMSTATE_RUN","mmstream/STREAMSTATE_STOP","mmstream/STREAM_STATE"]
old-location: dshow\stream_state.htm
tech.root: dshow
ms.assetid: 0be95819-0a42-4459-a891-194aacd26e2e
ms.date: 12/05/2018
ms.keywords: STREAMSTATE_RUN, STREAMSTATE_STOP, STREAM_STATE, STREAM_STATE enumeration [DirectShow], dshow.stream_state, mmstream/STREAMSTATE_RUN, mmstream/STREAMSTATE_STOP, mmstream/STREAM_STATE
req.header: mmstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: STREAM_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mmstream_0000_0000_0002
 - mmstream/__MIDL___MIDL_itf_mmstream_0000_0000_0002
 - STREAM_STATE
 - mmstream/STREAM_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmstream.h
api_name:
 - STREAM_STATE
---

# STREAM_STATE enumeration


## -description

<div class="alert"><b>Note</b>  This API is deprecated. New applications should not use it.</div>
<div> </div>
Describes the state of the stream.

## -enum-fields

### -field STREAMSTATE_STOP:0

Stop state.

### -field STREAMSTATE_RUN:1

Run state.

## -remarks

Change the state by calling the <a href="/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate">IMultiMediaStream::SetState</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/multimedia-streaming-types">Multimedia Streaming Enumeration Types</a>
