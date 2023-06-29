---
UID: NF:wmsdkidl.IWMIndexer.StartIndexing
title: IWMIndexer::StartIndexing (wmsdkidl.h)
description: The StartIndexing method initiates indexing.
helpviewer_keywords: ["IWMIndexer interface [windows Media Format]","StartIndexing method","IWMIndexer.StartIndexing","IWMIndexer::StartIndexing","IWMIndexerStartIndexing","StartIndexing","StartIndexing method [windows Media Format]","StartIndexing method [windows Media Format]","IWMIndexer interface","wmformat.iwmindexer_startindexing","wmsdkidl/IWMIndexer::StartIndexing"]
old-location: wmformat\iwmindexer_startindexing.htm
tech.root: wmformat
ms.assetid: 67dfb0df-4883-49e1-a085-0b78db3967d0
ms.date: 4/26/2023
ms.keywords: IWMIndexer interface [windows Media Format],StartIndexing method, IWMIndexer.StartIndexing, IWMIndexer::StartIndexing, IWMIndexerStartIndexing, StartIndexing, StartIndexing method [windows Media Format], StartIndexing method [windows Media Format],IWMIndexer interface, wmformat.iwmindexer_startindexing, wmsdkidl/IWMIndexer::StartIndexing
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMIndexer::StartIndexing
 - wmsdkidl/IWMIndexer::StartIndexing
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMIndexer.StartIndexing
---

# IWMIndexer::StartIndexing


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>StartIndexing</b> method initiates indexing. If you configure the indexer using the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmindexer2-configure">IWMIndexer2::Configure</a> method, <b>StartIndexing</b> creates an index based upon your configuration. When you use <b>StartIndexing</b> without first calling <b>Configure</b>, the indexer creates a default temporal index.

## -parameters

### -param pwszURL [in]

Pointer to a wide-character <b>null</b>-terminated string containing the URL or file name.

### -param pCallback [in]

Pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a> interface.

### -param pvContext [in]

Generic pointer, for use by the application.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>pwszURL</i> or <i>pCallback</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The method cannot start indexing in the current state.

</td>
</tr>
</table>

## -remarks

<b>StartIndexing</b> is an asynchronous call; it returns almost immediately and the application must wait for appropriate <b>OnStatus</b> calls to be sent to the callback function.

If you call <b>StartIndexing</b> for a file that is already indexed, the old index is discarded.

When the indexer successfully indexes a file, it will set some of the reserved attribute values as described in the following table.

<table>
<tr>
<th>Index type
            </th>
<th>Attributes set
            </th>
</tr>
<tr>
<td>WMT_IT_PRESENTATION_TIME</td>
<td>
g_wszWMSeekable

g_wszWMStridable, if a video stream is present.

</td>
</tr>
<tr>
<td>WMT_IT_FRAME_NUMBERS</td>
<td>
g_wszWMNumberOfFrames

g_wszWMSeekable

g_wszWMStridable

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer">IWMIndexer Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a>