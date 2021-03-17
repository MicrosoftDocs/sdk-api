---
UID: NF:mfidl.IMFFinalizableMediaSink.EndFinalize
title: IMFFinalizableMediaSink::EndFinalize (mfidl.h)
description: Completes an asynchronous finalize operation.
helpviewer_keywords: ["1b2a9b24-69da-41c7-8379-3f3d066d2582","EndFinalize","EndFinalize method [Media Foundation]","EndFinalize method [Media Foundation]","IMFFinalizableMediaSink interface","IMFFinalizableMediaSink interface [Media Foundation]","EndFinalize method","IMFFinalizableMediaSink.EndFinalize","IMFFinalizableMediaSink::EndFinalize","mf.imffinalizablemediasink_endfinalize","mfidl/IMFFinalizableMediaSink::EndFinalize"]
old-location: mf\imffinalizablemediasink_endfinalize.htm
tech.root: mf
ms.assetid: 1b2a9b24-69da-41c7-8379-3f3d066d2582
ms.date: 12/05/2018
ms.keywords: 1b2a9b24-69da-41c7-8379-3f3d066d2582, EndFinalize, EndFinalize method [Media Foundation], EndFinalize method [Media Foundation],IMFFinalizableMediaSink interface, IMFFinalizableMediaSink interface [Media Foundation],EndFinalize method, IMFFinalizableMediaSink.EndFinalize, IMFFinalizableMediaSink::EndFinalize, mf.imffinalizablemediasink_endfinalize, mfidl/IMFFinalizableMediaSink::EndFinalize
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFFinalizableMediaSink::EndFinalize
 - mfidl/IMFFinalizableMediaSink::EndFinalize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFFinalizableMediaSink.EndFinalize
---

# IMFFinalizableMediaSink::EndFinalize


## -description

Completes an asynchronous finalize operation.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

Call this method after the <a href="/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize">IMFFinalizableMediaSink::BeginFinalize</a> method completes asynchronously.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink">IMFFinalizableMediaSink</a>