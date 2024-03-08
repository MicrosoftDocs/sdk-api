---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetReceiveStreamSamples
title: IWMReaderAdvanced::SetReceiveStreamSamples (wmsdkidl.h)
description: The SetReceiveStreamSamples method specifies whether stream samples are delivered to the IWMReaderCallbackAdvanced::OnStreamSample callback.
helpviewer_keywords: ["IWMReaderAdvanced interface [windows Media Format]","SetReceiveStreamSamples method","IWMReaderAdvanced.SetReceiveStreamSamples","IWMReaderAdvanced::SetReceiveStreamSamples","IWMReaderAdvancedSetReceiveStreamSamples","SetReceiveStreamSamples","SetReceiveStreamSamples method [windows Media Format]","SetReceiveStreamSamples method [windows Media Format]","IWMReaderAdvanced interface","wmformat.iwmreaderadvanced_setreceivestreamsamples","wmsdkidl/IWMReaderAdvanced::SetReceiveStreamSamples"]
old-location: wmformat\iwmreaderadvanced_setreceivestreamsamples.htm
tech.root: wmformat
ms.assetid: 3fb39726-7f43-41ec-9ead-38456b5cd964
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetReceiveStreamSamples method, IWMReaderAdvanced.SetReceiveStreamSamples, IWMReaderAdvanced::SetReceiveStreamSamples, IWMReaderAdvancedSetReceiveStreamSamples, SetReceiveStreamSamples, SetReceiveStreamSamples method [windows Media Format], SetReceiveStreamSamples method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setreceivestreamsamples, wmsdkidl/IWMReaderAdvanced::SetReceiveStreamSamples
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
 - IWMReaderAdvanced::SetReceiveStreamSamples
 - wmsdkidl/IWMReaderAdvanced::SetReceiveStreamSamples
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
 - IWMReaderAdvanced.SetReceiveStreamSamples
---

# IWMReaderAdvanced::SetReceiveStreamSamples


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetReceiveStreamSamples</b> method specifies whether stream samples are delivered to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample">IWMReaderCallbackAdvanced::OnStreamSample</a> callback.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers are in the range of 1 through 63.

### -param fReceiveStreamSamples [in]

Boolean value that is True if stream samples are delivered.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
No callback interface has been specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PROTECTED_CONTENT</b></dt>
</dl>
</td>
<td width="60%">
Attempted read on a file protected by <a href="/windows/desktop/wmformat/wmformat-glossary">DRM</a>.

</td>
</tr>
</table>

## -remarks

Stream samples are samples received directly from the source file, and are not decompressed. If you receive compressed samples, you must either keep them compressed, or decompress them with your application. The Windows Media Format SDK does not provide methods to decompress samples once they have been removed from a file.

The application can register itself to receive samples directly from the Windows Media streams rather than letting the reader decompress them first. To do this, the object implementing <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback</a> (supplied by the application) must support <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced</a>. To determine which streams are in an ASF file, and what their stream numbers are, call <b>QueryInterface</b> using the reader object to access the <a href="/windows/desktop/wmformat/iwmprofile">IWMProfile</a> interface, and examine the streams in the profile.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getreceivestreamsamples">IWMReaderAdvanced::GetReceiveStreamSamples</a>