---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetStreamsSelected
title: IWMReaderAdvanced::SetStreamsSelected (wmsdkidl.h)
description: The SetStreamsSelected method specifies which streams are selected when manual stream selection is enabled.
helpviewer_keywords: ["IWMReaderAdvanced interface [windows Media Format]","SetStreamsSelected method","IWMReaderAdvanced.SetStreamsSelected","IWMReaderAdvanced::SetStreamsSelected","IWMReaderAdvancedSetStreamsSelected","SetStreamsSelected","SetStreamsSelected method [windows Media Format]","SetStreamsSelected method [windows Media Format]","IWMReaderAdvanced interface","wmformat.iwmreaderadvanced_setstreamsselected","wmsdkidl/IWMReaderAdvanced::SetStreamsSelected"]
old-location: wmformat\iwmreaderadvanced_setstreamsselected.htm
tech.root: wmformat
ms.assetid: 921ab9fe-757f-4856-9fbc-b615bf92d90f
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetStreamsSelected method, IWMReaderAdvanced.SetStreamsSelected, IWMReaderAdvanced::SetStreamsSelected, IWMReaderAdvancedSetStreamsSelected, SetStreamsSelected, SetStreamsSelected method [windows Media Format], SetStreamsSelected method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setstreamsselected, wmsdkidl/IWMReaderAdvanced::SetStreamsSelected
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
 - IWMReaderAdvanced::SetStreamsSelected
 - wmsdkidl/IWMReaderAdvanced::SetStreamsSelected
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
 - IWMReaderAdvanced.SetStreamsSelected
---

# IWMReaderAdvanced::SetStreamsSelected


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetStreamsSelected</b> method specifies which streams are selected when manual stream selection is enabled.

## -parameters

### -param cStreamCount [in]

<b>WORD</b> containing the count of stream numbers in the <i>pwStreamNumbers</i> array.

### -param pwStreamNumbers [in]

Pointer to an array containing the stream numbers. Stream numbers are in the range of 1 through 63.

### -param pSelections [in]

Pointer to an array, of equal length to <i>pwStreamNumbers</i>, with each entry containing one member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_stream_selection">WMT_STREAM_SELECTION</a> enumeration type.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>

## -remarks

This method enables the selected state of multiple streams to be changed simultaneously. Multiple streams can then be turned on or off at the exact time required. For this reason, the parameters of this method and the <b>GetStreamSelected</b> method are not identical.

When selecting streams manually, you should select only one stream at a time from each set of mutually exclusive streams in a file. The SDK does not prevent you from selecting multiple mutually exclusive streams, but the samples for all mutually exclusive streams will be delivered to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">IWMReaderCallback::OnSample</a> using the same output number. This makes it difficult to differentiate between samples from the various streams.

To deliver samples by stream number, you must receive uncompressed stream samples. You can receive stream samples for a specific stream by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples">IWMReaderAdvanced::SetReceiveStreamSamples</a>. You must also implement <b>IWMReaderCallbackAdvanced::OnStreamSample</b>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected">IWMReaderAdvanced::GetStreamSelected</a>



<a href="/windows/desktop/wmformat/to-use-manual-stream-selection">To Use Manual Stream Selection</a>