---
UID: NF:wmsdkidl.IWMSyncReader.GetReadStreamSamples
title: IWMSyncReader::GetReadStreamSamples (wmsdkidl.h)
description: The GetReadStreamSamples method ascertains whether a stream is configured to deliver compressed samples.
helpviewer_keywords: ["GetReadStreamSamples","GetReadStreamSamples method [windows Media Format]","GetReadStreamSamples method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","GetReadStreamSamples method","IWMSyncReader.GetReadStreamSamples","IWMSyncReader::GetReadStreamSamples","IWMSyncReaderGetReadStreamSamples","wmformat.iwmsyncreader_getreadstreamsamples","wmsdkidl/IWMSyncReader::GetReadStreamSamples"]
old-location: wmformat\iwmsyncreader_getreadstreamsamples.htm
tech.root: wmformat
ms.assetid: cb903723-fd4b-4b1c-aa2f-e3c9f74dcebd
ms.date: 4/26/2023
ms.keywords: GetReadStreamSamples, GetReadStreamSamples method [windows Media Format], GetReadStreamSamples method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetReadStreamSamples method, IWMSyncReader.GetReadStreamSamples, IWMSyncReader::GetReadStreamSamples, IWMSyncReaderGetReadStreamSamples, wmformat.iwmsyncreader_getreadstreamsamples, wmsdkidl/IWMSyncReader::GetReadStreamSamples
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
 - IWMSyncReader::GetReadStreamSamples
 - wmsdkidl/IWMSyncReader::GetReadStreamSamples
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
 - IWMSyncReader.GetReadStreamSamples
---

# IWMSyncReader::GetReadStreamSamples


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetReadStreamSamples</b> method ascertains whether a stream is configured to deliver compressed samples.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

### -param pfCompressed [out]

Pointer to a flag that receives the status of compressed delivery for the stream specified.

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
<i>pfCompressed</i> is <b>NULL</b>.

OR

<i>wStreamNum</i> specifies an invalid stream number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
No file is open in the synchronous reader.

</td>
</tr>
</table>

## -remarks

To configure a stream to deliver compressed samples, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples">IWMSyncReader::SetReadStreamSamples</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>