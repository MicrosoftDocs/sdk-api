---
UID: NF:mmstream.IMediaStream.CreateSharedSample
title: IMediaStream::CreateSharedSample (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. Creates a new stream sample that shares the same backing object as the existing sample.
helpviewer_keywords: ["CreateSharedSample","CreateSharedSample method [DirectShow]","CreateSharedSample method [DirectShow]","IMediaStream interface","IMediaStream interface [DirectShow]","CreateSharedSample method","IMediaStream.CreateSharedSample","IMediaStream::CreateSharedSample","IMediaStreamCreateSharedSample","dshow.imediastream_createsharedsample","mmstream/IMediaStream::CreateSharedSample"]
old-location: dshow\imediastream_createsharedsample.htm
tech.root: dshow
ms.assetid: acefa476-e607-45b4-854d-840e948af029
ms.date: 12/05/2018
ms.keywords: CreateSharedSample, CreateSharedSample method [DirectShow], CreateSharedSample method [DirectShow],IMediaStream interface, IMediaStream interface [DirectShow],CreateSharedSample method, IMediaStream.CreateSharedSample, IMediaStream::CreateSharedSample, IMediaStreamCreateSharedSample, dshow.imediastream_createsharedsample, mmstream/IMediaStream::CreateSharedSample
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaStream::CreateSharedSample
 - mmstream/IMediaStream::CreateSharedSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMediaStream.CreateSharedSample
---

# IMediaStream::CreateSharedSample


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Creates a new stream sample that shares the same backing object as the existing sample.

## -parameters

### -param pExistingSample [in]

Pointer to the existing sample.

### -param dwFlags [in]

Reserved for flag data. Must be zero.

### -param ppNewSample [out]

Address of a pointer to an <a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a> interface that will point to the newly created shared sample.

## -returns

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There isn't enough memory available to create the sample.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_INCOMPATIBLE</b></dt>
</dl>
</td>
<td width="60%">
The existing sample isn't compatible with the specified media stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success; <i>ppNewSample</i> points to the newly created sample.

</td>
</tr>
</table>

## -remarks

This method calls <b>IUnknown::QueryInterface</b> on the existing sample to retrieve the media type-specific information, which it uses to create the shared sample.

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream Interface</a>