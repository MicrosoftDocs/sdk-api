---
UID: NF:wmsdkidl.IWMWriterPostViewCallback.OnPostViewSample
title: IWMWriterPostViewCallback::OnPostViewSample (wmsdkidl.h)
description: The OnPostViewSample method is called when new postview data is available. The application implements this method.
helpviewer_keywords: ["IWMWriterPostViewCallback interface [windows Media Format]","OnPostViewSample method","IWMWriterPostViewCallback.OnPostViewSample","IWMWriterPostViewCallback::OnPostViewSample","IWMWriterPostViewCallbackOnPostViewSample","OnPostViewSample","OnPostViewSample method [windows Media Format]","OnPostViewSample method [windows Media Format]","IWMWriterPostViewCallback interface","wmformat.iwmwriterpostviewcallback_onpostviewsample","wmsdkidl/IWMWriterPostViewCallback::OnPostViewSample"]
old-location: wmformat\iwmwriterpostviewcallback_onpostviewsample.htm
tech.root: wmformat
ms.assetid: 5d29a746-70fe-495e-a7f2-dbf085829496
ms.date: 4/26/2023
ms.keywords: IWMWriterPostViewCallback interface [windows Media Format],OnPostViewSample method, IWMWriterPostViewCallback.OnPostViewSample, IWMWriterPostViewCallback::OnPostViewSample, IWMWriterPostViewCallbackOnPostViewSample, OnPostViewSample, OnPostViewSample method [windows Media Format], OnPostViewSample method [windows Media Format],IWMWriterPostViewCallback interface, wmformat.iwmwriterpostviewcallback_onpostviewsample, wmsdkidl/IWMWriterPostViewCallback::OnPostViewSample
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
 - IWMWriterPostViewCallback::OnPostViewSample
 - wmsdkidl/IWMWriterPostViewCallback::OnPostViewSample
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
 - IWMWriterPostViewCallback.OnPostViewSample
---

# IWMWriterPostViewCallback::OnPostViewSample


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>OnPostViewSample</b> method is called when new postview data is available. The application implements this method.

## -parameters

### -param wStreamNumber [in]

<b>WORD</b> containing the stream number.

### -param cnsSampleTime [in]

Sample time, in 100-nanosecond units.

### -param cnsSampleDuration [in]

Sample duration, in 100-nanosecond units. This will usually be 10000 (1 millisecond).

### -param dwFlags [in]

<b>DWORD</b> containing none, one, or more of the following flags.

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
<td>This is basically the same as a key frame. It indicates a good point to go to during a seek, for example.</td>
</tr>
<tr>
<td>WM_SF_DISCONTINUITY</td>
<td>The data stream has a gap in it, which could be due to a seek, a network loss, or some other reason. This can be useful extra information for an application such as a codec or renderer. The flag is set on the first piece of data following the gap.</td>
</tr>
<tr>
<td>WM_SF_DATALOSS</td>
<td>Some data has been lost between the previous sample and the sample with this flag set.</td>
</tr>
</table>

### -param pSample [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface on an object that contains the sample.

### -param pvContext [in]

Generic pointer, for use by the application.

## -returns

This method is implemented by the application. It should return S_OK.

## -remarks

Postview data is available only for video.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">IWMReaderCallback::OnSample</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback">IWMWriterPostViewCallback Interface</a>