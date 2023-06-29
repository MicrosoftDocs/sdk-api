---
UID: NF:wmsdkidl.IWMSyncReader.SetStreamsSelected
title: IWMSyncReader::SetStreamsSelected (wmsdkidl.h)
description: The SetStreamsSelected method configures the samples to be delivered from a list of streams. Each stream can be set to deliver all samples, no samples, or only cleanpoint samples.
helpviewer_keywords: ["IWMSyncReader interface [windows Media Format]","SetStreamsSelected method","IWMSyncReader.SetStreamsSelected","IWMSyncReader::SetStreamsSelected","IWMSyncReaderSetStreamsSelected","SetStreamsSelected","SetStreamsSelected method [windows Media Format]","SetStreamsSelected method [windows Media Format]","IWMSyncReader interface","wmformat.iwmsyncreader_setstreamsselected","wmsdkidl/IWMSyncReader::SetStreamsSelected"]
old-location: wmformat\iwmsyncreader_setstreamsselected.htm
tech.root: wmformat
ms.assetid: d62a61cb-3b5a-4ce8-9677-92e280449d26
ms.date: 4/26/2023
ms.keywords: IWMSyncReader interface [windows Media Format],SetStreamsSelected method, IWMSyncReader.SetStreamsSelected, IWMSyncReader::SetStreamsSelected, IWMSyncReaderSetStreamsSelected, SetStreamsSelected, SetStreamsSelected method [windows Media Format], SetStreamsSelected method [windows Media Format],IWMSyncReader interface, wmformat.iwmsyncreader_setstreamsselected, wmsdkidl/IWMSyncReader::SetStreamsSelected
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMSyncReader::SetStreamsSelected
 - wmsdkidl/IWMSyncReader::SetStreamsSelected
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
 - IWMSyncReader.SetStreamsSelected
---

# IWMSyncReader::SetStreamsSelected


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetStreamsSelected</b> method configures the samples to be delivered from a list of streams. Each stream can be set to deliver all samples, no samples, or only <a href="/windows/desktop/wmformat/wmformat-glossary">cleanpoint</a> samples.

## -parameters

### -param cStreamCount [in]

Count of streams listed at <i>pwStreamNumbers</i>.

### -param pwStreamNumbers [in]

Pointer to an array of <b>WORD</b> values containing the stream numbers.

### -param pSelections [in]

Pointer to an array of <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_stream_selection">WMT_STREAM_SELECTION</a> enumeration values. These values correspond with the stream numbers listed at <i>pwStreamNumbers</i>. Each value specifies the samples to deliver for the appropriate stream.

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
<i>pwStreamNumbers</i> or <i>pSelections</i> is <b>NULL</b>.

OR

<i>cStreamCount</i> is zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
No file is loaded in the synchronous reader.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory for an internal object.

</td>
</tr>
</table>

## -remarks

You can call <b>SetStreamsSelects</b> at any time after a file has been loaded into the synchronous reader. You can continue making calls as needed during playback.

This method is identical to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected">IWMReaderAdvanced::SetStreamsSelected</a> except that, in the synchronous reader, stream selection is always manual. Also, because <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample">IWMSyncReader::GetNextSample</a> includes a stream number output, you can select as many mutually exclusive streams as you like and receive samples for them.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>