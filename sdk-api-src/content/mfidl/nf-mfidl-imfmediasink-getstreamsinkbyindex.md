---
UID: NF:mfidl.IMFMediaSink.GetStreamSinkByIndex
title: IMFMediaSink::GetStreamSinkByIndex (mfidl.h)
description: Gets a stream sink, specified by index.
helpviewer_keywords: ["01604801-1566-410c-b23a-0568c7298868","GetStreamSinkByIndex","GetStreamSinkByIndex method [Media Foundation]","GetStreamSinkByIndex method [Media Foundation]","IMFMediaSink interface","IMFMediaSink interface [Media Foundation]","GetStreamSinkByIndex method","IMFMediaSink.GetStreamSinkByIndex","IMFMediaSink::GetStreamSinkByIndex","mf.imfmediasink_getstreamsinkbyindex","mfidl/IMFMediaSink::GetStreamSinkByIndex"]
old-location: mf\imfmediasink_getstreamsinkbyindex.htm
tech.root: medfound
ms.assetid: 01604801-1566-410c-b23a-0568c7298868
ms.date: 12/05/2018
ms.keywords: 01604801-1566-410c-b23a-0568c7298868, GetStreamSinkByIndex, GetStreamSinkByIndex method [Media Foundation], GetStreamSinkByIndex method [Media Foundation],IMFMediaSink interface, IMFMediaSink interface [Media Foundation],GetStreamSinkByIndex method, IMFMediaSink.GetStreamSinkByIndex, IMFMediaSink::GetStreamSinkByIndex, mf.imfmediasink_getstreamsinkbyindex, mfidl/IMFMediaSink::GetStreamSinkByIndex
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
 - IMFMediaSink::GetStreamSinkByIndex
 - mfidl/IMFMediaSink::GetStreamSinkByIndex
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
 - IMFMediaSink.GetStreamSinkByIndex
---

# IMFMediaSink::GetStreamSinkByIndex


## -description

Gets a stream sink, specified by index.

## -parameters

### -param dwIndex [in]

Zero-based index of the stream. To get the number of streams, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount">IMFMediaSink::GetStreamSinkCount</a>.

### -param ppStreamSink [out]

Receives a pointer to the stream's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink">IMFStreamSink</a> interface. The caller must release the interface.

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
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid index.

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

## -remarks

Enumerating stream sinks is not a thread-safe operation, because stream sinks can be added or removed between calls to this method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>