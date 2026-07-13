---
UID: NN:mfreadwrite.IMFSinkWriterCallback
title: IMFSinkWriterCallback (mfreadwrite.h)
description: Callback interface for the Microsoft Media Foundation sink writer.
helpviewer_keywords: ["IMFSinkWriterCallback","IMFSinkWriterCallback interface [Media Foundation]","IMFSinkWriterCallback interface [Media Foundation]","described","mf.imfsinkwritercallback","mfreadwrite/IMFSinkWriterCallback"]
old-location: mf\imfsinkwritercallback.htm
tech.root: mf
ms.assetid: fa0295e6-473d-4304-9a7b-24584cade0a0
ms.date: 12/05/2018
ms.keywords: IMFSinkWriterCallback, IMFSinkWriterCallback interface [Media Foundation], IMFSinkWriterCallback interface [Media Foundation],described, mf.imfsinkwritercallback, mfreadwrite/IMFSinkWriterCallback
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IMFSinkWriterCallback
 - mfreadwrite/IMFSinkWriterCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSinkWriterCallback
---

# IMFSinkWriterCallback interface


## -description

Callback interface for the Microsoft Media Foundation sink writer.

## -inheritance

The <b>IMFSinkWriterCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSinkWriterCallback</b> also has these types of members:

## -remarks

Set the callback pointer by setting the <a href="/windows/desktop/medfound/mf-sink-writer-async-callback">MF_SINK_WRITER_ASYNC_CALLBACK</a> attribute when you first create the sink writer.



The callback methods can be called from any thread, so an object that implements this interface must be thread-safe.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>
