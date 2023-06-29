---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetReceiveStreamSamples
title: IWMReaderAdvanced::GetReceiveStreamSamples (wmsdkidl.h)
description: The GetReceiveStreamSamples method ascertains whether stream samples are delivered to the IWMReaderCallbackAdvanced::OnStreamSample call.
helpviewer_keywords: ["GetReceiveStreamSamples","GetReceiveStreamSamples method [windows Media Format]","GetReceiveStreamSamples method [windows Media Format]","IWMReaderAdvanced interface","IWMReaderAdvanced interface [windows Media Format]","GetReceiveStreamSamples method","IWMReaderAdvanced.GetReceiveStreamSamples","IWMReaderAdvanced::GetReceiveStreamSamples","IWMReaderAdvancedGetReceiveStreamSamples","wmformat.iwmreaderadvanced_getreceivestreamsamples","wmsdkidl/IWMReaderAdvanced::GetReceiveStreamSamples"]
old-location: wmformat\iwmreaderadvanced_getreceivestreamsamples.htm
tech.root: wmformat
ms.assetid: cdb76a25-fc30-4be2-a54e-928050699e58
ms.date: 4/26/2023
ms.keywords: GetReceiveStreamSamples, GetReceiveStreamSamples method [windows Media Format], GetReceiveStreamSamples method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetReceiveStreamSamples method, IWMReaderAdvanced.GetReceiveStreamSamples, IWMReaderAdvanced::GetReceiveStreamSamples, IWMReaderAdvancedGetReceiveStreamSamples, wmformat.iwmreaderadvanced_getreceivestreamsamples, wmsdkidl/IWMReaderAdvanced::GetReceiveStreamSamples
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
 - IWMReaderAdvanced::GetReceiveStreamSamples
 - wmsdkidl/IWMReaderAdvanced::GetReceiveStreamSamples
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
 - IWMReaderAdvanced.GetReceiveStreamSamples
---

# IWMReaderAdvanced::GetReceiveStreamSamples


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetReceiveStreamSamples</b> method ascertains whether stream samples are delivered to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample">IWMReaderCallbackAdvanced::OnStreamSample</a> call.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers are in the range of 1 through 63.

### -param pfReceiveStreamSamples [out]

Pointer to a Boolean value that is set to True if stream samples are delivered to <b>OnStreamSample</b>.

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
The <i>pfReceiveStreamSamples</i> parameter is <b>NULL</b>, or the stream number is not valid.

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

Stream samples are samples received directly from the source file, and are not decompressed. If you receive compressed samples, you must either keep them compressed, or decompress them with your application. The Windows Media Format SDK does not provide methods to decompress samples once they have been removed from a file.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples">IWMReaderAdvanced::SetReceiveStreamSamples</a>