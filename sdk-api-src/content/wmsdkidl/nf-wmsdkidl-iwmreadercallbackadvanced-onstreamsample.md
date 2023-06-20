---
UID: NF:wmsdkidl.IWMReaderCallbackAdvanced.OnStreamSample
title: IWMReaderCallbackAdvanced::OnStreamSample (wmsdkidl.h)
description: The OnStreamSample method delivers stream samples from the source file without decompressing them first.
helpviewer_keywords: ["IWMReaderCallbackAdvanced interface [windows Media Format]","OnStreamSample method","IWMReaderCallbackAdvanced.OnStreamSample","IWMReaderCallbackAdvanced::OnStreamSample","IWMReaderCallbackAdvancedOnStreamSample","OnStreamSample","OnStreamSample method [windows Media Format]","OnStreamSample method [windows Media Format]","IWMReaderCallbackAdvanced interface","wmformat.iwmreadercallbackadvanced_onstreamsample","wmsdkidl/IWMReaderCallbackAdvanced::OnStreamSample"]
old-location: wmformat\iwmreadercallbackadvanced_onstreamsample.htm
tech.root: wmformat
ms.assetid: 6bfdd903-a3a4-4ef4-b88a-4d24c9c0f4b8
ms.date: 4/26/2023
ms.keywords: IWMReaderCallbackAdvanced interface [windows Media Format],OnStreamSample method, IWMReaderCallbackAdvanced.OnStreamSample, IWMReaderCallbackAdvanced::OnStreamSample, IWMReaderCallbackAdvancedOnStreamSample, OnStreamSample, OnStreamSample method [windows Media Format], OnStreamSample method [windows Media Format],IWMReaderCallbackAdvanced interface, wmformat.iwmreadercallbackadvanced_onstreamsample, wmsdkidl/IWMReaderCallbackAdvanced::OnStreamSample
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMReaderCallbackAdvanced::OnStreamSample
 - wmsdkidl/IWMReaderCallbackAdvanced::OnStreamSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsdkidl.h
api_name:
 - IWMReaderCallbackAdvanced.OnStreamSample
---

# IWMReaderCallbackAdvanced::OnStreamSample


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>OnStreamSample</b> method delivers stream samples from the source file without decompressing them first.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number.

### -param cnsSampleTime [in]

<b>QWORD</b> containing the sample time, in 100-nanosecond units.

### -param cnsSampleDuration [in]

<b>QWORD</b> containing the sample duration, in 100-nanosecond units.

### -param dwFlags [in]

The flags that can be specified have the following uses.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>No flag set</td>
<td>None of the conditions for the other flags applies. For example, a <a href="/windows/desktop/wmformat/wmformat-glossary">delta frame</a> in most cases would not have any flags set for it.</td>
</tr>
<tr>
<td>WM_SF_CLEANPOINT</td>
<td>This is the same as a <a href="/windows/desktop/wmformat/wmformat-glossary">key frame</a>. It indicates a good point to go to during a seek, for example.</td>
</tr>
<tr>
<td>WM_SF_DISCONTINUITY</td>
<td>The data stream has a gap in it, which could be due to a seek, a network loss, or other reason. This can be useful extra information for an application such as a codec or renderer. The flag is set on the first piece of data following the gap.</td>
</tr>
<tr>
<td>WM_SF_DATALOSS</td>
<td>Some data has been lost between the previous sample, and the sample with this flag set.</td>
</tr>
</table>

### -param pSample [in]

Pointer to a sample stored in an <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface. The reader calls <b>SAFE_RELEASE</b> on this pointer after your <b>OnStreamSample</b> method returns. You can call <b>AddRef</b> on this pointer if you need to keep a reference count on the buffer. Do not call <b>Release</b> on this pointer unless you have called <b>AddRef</b>.

### -param pvContext [in]

Generic pointer, for use by the application.

## -returns

To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="/windows/desktop/wmformat/error-codes">Error Codes</a>.

## -remarks

When using the asynchronous reader, only compressed samples can be delivered for a stream number. If you want to retrieve uncompressed samples by stream number, you should use the synchronous reader.

There are many reasons why you might want to retrieve compressed samples. The most common use is to transfer a stream from one ASF file to another.

If you receive compressed samples, you must either keep them compressed, or decompress them with your application. The Windows Media Format SDK does not provide methods to decompress samples once they have been removed from a file.

This method is not able to deliver secure content. If protected content is used, the method will return NS_E_PROTECTEDCONTENT.

The samples delivered by this method are compressed, but are in all other ways exactly the same as samples delivered through <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">IWMReaderCallback::OnSample</a>.

To get samples for a particular stream, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples">IWMReaderAdvanced::SetReceiveStreamSamples</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced Interface</a>