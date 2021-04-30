---
UID: NF:mfidl.IMFMediaStream.GetMediaSource
title: IMFMediaStream::GetMediaSource (mfidl.h)
description: Retrieves a pointer to the media source that created this media stream.
helpviewer_keywords: ["GetMediaSource","GetMediaSource method [Media Foundation]","GetMediaSource method [Media Foundation]","IMFMediaStream interface","IMFMediaStream interface [Media Foundation]","GetMediaSource method","IMFMediaStream.GetMediaSource","IMFMediaStream::GetMediaSource","ffca44ca-14ae-4f93-a719-9012a8151a7a","mf.imfmediastream_getmediasource","mfidl/IMFMediaStream::GetMediaSource"]
old-location: mf\imfmediastream_getmediasource.htm
tech.root: mf
ms.assetid: ffca44ca-14ae-4f93-a719-9012a8151a7a
ms.date: 12/05/2018
ms.keywords: GetMediaSource, GetMediaSource method [Media Foundation], GetMediaSource method [Media Foundation],IMFMediaStream interface, IMFMediaStream interface [Media Foundation],GetMediaSource method, IMFMediaStream.GetMediaSource, IMFMediaStream::GetMediaSource, ffca44ca-14ae-4f93-a719-9012a8151a7a, mf.imfmediastream_getmediasource, mfidl/IMFMediaStream::GetMediaSource
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaStream::GetMediaSource
 - mfidl/IMFMediaStream::GetMediaSource
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
 - IMFMediaStream.GetMediaSource
---

# IMFMediaStream::GetMediaSource


## -description

Retrieves a pointer to the media source that created this media stream.

## -parameters

### -param ppMediaSource [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> interface of the media source. The caller must release the interface.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media source's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown">Shutdown</a> method has been called.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediastream">IMFMediaStream</a>



<a href="/windows/desktop/medfound/media-sources">Media Sources</a>