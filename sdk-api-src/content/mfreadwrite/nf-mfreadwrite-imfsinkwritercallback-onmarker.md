---
UID: NF:mfreadwrite.IMFSinkWriterCallback.OnMarker
title: IMFSinkWriterCallback::OnMarker (mfreadwrite.h)
description: Called when the IMFSinkWriter::PlaceMarker method completes.
helpviewer_keywords: ["IMFSinkWriterCallback interface [Media Foundation]","OnMarker method","IMFSinkWriterCallback.OnMarker","IMFSinkWriterCallback::OnMarker","OnMarker","OnMarker method [Media Foundation]","OnMarker method [Media Foundation]","IMFSinkWriterCallback interface","mf.imfsinkwritercallback_onmarker","mfreadwrite/IMFSinkWriterCallback::OnMarker"]
old-location: mf\imfsinkwritercallback_onmarker.htm
tech.root: mf
ms.assetid: 5b1ca6a7-c2bc-4b30-aa86-05bd4ccc052c
ms.date: 12/05/2018
ms.keywords: IMFSinkWriterCallback interface [Media Foundation],OnMarker method, IMFSinkWriterCallback.OnMarker, IMFSinkWriterCallback::OnMarker, OnMarker, OnMarker method [Media Foundation], OnMarker method [Media Foundation],IMFSinkWriterCallback interface, mf.imfsinkwritercallback_onmarker, mfreadwrite/IMFSinkWriterCallback::OnMarker
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
 - IMFSinkWriterCallback::OnMarker
 - mfreadwrite/IMFSinkWriterCallback::OnMarker
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
 - IMFSinkWriterCallback.OnMarker
---

# IMFSinkWriterCallback::OnMarker


## -description

Called when the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-placemarker">IMFSinkWriter::PlaceMarker</a> method completes.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of the stream. This parameter equals the value of the <i>dwStreamIndex</i> parameter in the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-placemarker">PlaceMarker</a> method.

### -param pvContext [in]

The application-defined value that was given in the <i>pvContext</i> parameter in the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-placemarker">PlaceMarker</a> method.

## -returns

Returns an <b>HRESULT</b> value. Currently, the sink writer ignores the return value.

## -remarks

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback">IMFSinkWriterCallback</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>