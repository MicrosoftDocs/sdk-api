---
UID: NF:wmsdkidl.IWMWriterSink.OnEndWriting
title: IWMWriterSink::OnEndWriting (wmsdkidl.h)
description: The OnEndWriting method is called by the writer when writing is complete. This method should conclude operations for your sink. For example, the writer file sink closes and indexes the file.
helpviewer_keywords: ["IWMWriterSink interface [windows Media Format]","OnEndWriting method","IWMWriterSink.OnEndWriting","IWMWriterSink::OnEndWriting","IWMWriterSinkOnEndWriting","OnEndWriting","OnEndWriting method [windows Media Format]","OnEndWriting method [windows Media Format]","IWMWriterSink interface","wmformat.iwmwritersink_onendwriting","wmsdkidl/IWMWriterSink::OnEndWriting"]
old-location: wmformat\iwmwritersink_onendwriting.htm
tech.root: wmformat
ms.assetid: e5f653cc-e756-4f33-a6ce-3158e83129c8
ms.date: 4/26/2023
ms.keywords: IWMWriterSink interface [windows Media Format],OnEndWriting method, IWMWriterSink.OnEndWriting, IWMWriterSink::OnEndWriting, IWMWriterSinkOnEndWriting, OnEndWriting, OnEndWriting method [windows Media Format], OnEndWriting method [windows Media Format],IWMWriterSink interface, wmformat.iwmwritersink_onendwriting, wmsdkidl/IWMWriterSink::OnEndWriting
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
 - IWMWriterSink::OnEndWriting
 - wmsdkidl/IWMWriterSink::OnEndWriting
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
 - IWMWriterSink.OnEndWriting
---

# IWMWriterSink::OnEndWriting


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>OnEndWriting</b> method is called by the writer when writing is complete. This method should conclude operations for your sink. For example, the writer file sink closes and indexes the file.



## -returns

This method is implemented by the application. It should always return S_OK.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>
