---
UID: NF:mfidl.IMFMediaSink.GetStreamSinkCount
title: IMFMediaSink::GetStreamSinkCount (mfidl.h)
description: Gets the number of stream sinks on this media sink.
helpviewer_keywords: ["GetStreamSinkCount","GetStreamSinkCount method [Media Foundation]","GetStreamSinkCount method [Media Foundation]","IMFMediaSink interface","IMFMediaSink interface [Media Foundation]","GetStreamSinkCount method","IMFMediaSink.GetStreamSinkCount","IMFMediaSink::GetStreamSinkCount","bf4b5713-586c-4b12-80a1-4452eec63e32","mf.imfmediasink_getstreamsinkcount","mfidl/IMFMediaSink::GetStreamSinkCount"]
old-location: mf\imfmediasink_getstreamsinkcount.htm
tech.root: mf
ms.assetid: bf4b5713-586c-4b12-80a1-4452eec63e32
ms.date: 12/05/2018
ms.keywords: GetStreamSinkCount, GetStreamSinkCount method [Media Foundation], GetStreamSinkCount method [Media Foundation],IMFMediaSink interface, IMFMediaSink interface [Media Foundation],GetStreamSinkCount method, IMFMediaSink.GetStreamSinkCount, IMFMediaSink::GetStreamSinkCount, bf4b5713-586c-4b12-80a1-4452eec63e32, mf.imfmediasink_getstreamsinkcount, mfidl/IMFMediaSink::GetStreamSinkCount
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
 - IMFMediaSink::GetStreamSinkCount
 - mfidl/IMFMediaSink::GetStreamSinkCount
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
 - IMFMediaSink.GetStreamSinkCount
---

# IMFMediaSink::GetStreamSinkCount


## -description

Gets the number of stream sinks on this media sink.

## -parameters

### -param pcStreamSinkCount [out]

Receives the number of stream sinks.

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
The media sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown">Shutdown</a> method has been called.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>