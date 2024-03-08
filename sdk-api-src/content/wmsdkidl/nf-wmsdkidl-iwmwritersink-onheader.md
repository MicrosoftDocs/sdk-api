---
UID: NF:wmsdkidl.IWMWriterSink.OnHeader
title: IWMWriterSink::OnHeader (wmsdkidl.h)
description: The OnHeader method is called by the writer when the ASF header is ready for the sink.
helpviewer_keywords: ["IWMWriterSink interface [windows Media Format]","OnHeader method","IWMWriterSink.OnHeader","IWMWriterSink::OnHeader","IWMWriterSinkOnHeader","OnHeader","OnHeader method [windows Media Format]","OnHeader method [windows Media Format]","IWMWriterSink interface","wmformat.iwmwritersink_onheader","wmsdkidl/IWMWriterSink::OnHeader"]
old-location: wmformat\iwmwritersink_onheader.htm
tech.root: wmformat
ms.assetid: 97b1dbd0-a555-40d3-b2f0-3a363a6ce168
ms.date: 4/26/2023
ms.keywords: IWMWriterSink interface [windows Media Format],OnHeader method, IWMWriterSink.OnHeader, IWMWriterSink::OnHeader, IWMWriterSinkOnHeader, OnHeader, OnHeader method [windows Media Format], OnHeader method [windows Media Format],IWMWriterSink interface, wmformat.iwmwritersink_onheader, wmsdkidl/IWMWriterSink::OnHeader
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
 - IWMWriterSink::OnHeader
 - wmsdkidl/IWMWriterSink::OnHeader
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
 - IWMWriterSink.OnHeader
---

# IWMWriterSink::OnHeader


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>OnHeader</b> method is called by the writer when the ASF header is ready for the sink.

## -parameters

### -param pHeader [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface on an object containing the ASF header.

## -returns

This method is implemented by the application. It should always return S_OK.

## -remarks

The ASF header will always be sent before any data units, as the header is required for reading the content. The writer may send the header more than once for a given file. If possible, your sink should write any headers received.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>