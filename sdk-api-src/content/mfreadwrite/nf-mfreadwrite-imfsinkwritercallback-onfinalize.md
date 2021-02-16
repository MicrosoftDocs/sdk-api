---
UID: NF:mfreadwrite.IMFSinkWriterCallback.OnFinalize
title: IMFSinkWriterCallback::OnFinalize (mfreadwrite.h)
description: Called when the IMFSinkWriter::Finalize method completes.
helpviewer_keywords: ["IMFSinkWriterCallback interface [Media Foundation]","OnFinalize method","IMFSinkWriterCallback.OnFinalize","IMFSinkWriterCallback::OnFinalize","OnFinalize","OnFinalize method [Media Foundation]","OnFinalize method [Media Foundation]","IMFSinkWriterCallback interface","mf.imfsinkwritercallback_onfinalize","mfreadwrite/IMFSinkWriterCallback::OnFinalize"]
old-location: mf\imfsinkwritercallback_onfinalize.htm
tech.root: mf
ms.assetid: 9da7bb55-bf9f-4579-ae8e-b33ce5461950
ms.date: 12/05/2018
ms.keywords: IMFSinkWriterCallback interface [Media Foundation],OnFinalize method, IMFSinkWriterCallback.OnFinalize, IMFSinkWriterCallback::OnFinalize, OnFinalize, OnFinalize method [Media Foundation], OnFinalize method [Media Foundation],IMFSinkWriterCallback interface, mf.imfsinkwritercallback_onfinalize, mfreadwrite/IMFSinkWriterCallback::OnFinalize
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
 - IMFSinkWriterCallback::OnFinalize
 - mfreadwrite/IMFSinkWriterCallback::OnFinalize
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
 - IMFSinkWriterCallback.OnFinalize
---

# IMFSinkWriterCallback::OnFinalize


## -description

Called when the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize">IMFSinkWriter::Finalize</a> method completes.

## -parameters

### -param hrStatus [in]

The status code for the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize">Finalize</a> operation. If the value is an error code, the output file might be invalid.

## -returns

Returns an <b>HRESULT</b> value. Currently, the sink writer ignores the return value.

## -remarks

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback">IMFSinkWriterCallback</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>