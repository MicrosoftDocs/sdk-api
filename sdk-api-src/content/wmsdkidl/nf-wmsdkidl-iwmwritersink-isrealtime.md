---
UID: NF:wmsdkidl.IWMWriterSink.IsRealTime
title: IWMWriterSink::IsRealTime (wmsdkidl.h)
description: The IsRealTime is called by the writer to determine whether the sink needs data units to be delivered in real time. It is up to you to decide whether your custom sink requires real-time delivery.
helpviewer_keywords: ["IWMWriterSink interface [windows Media Format]","IsRealTime method","IWMWriterSink.IsRealTime","IWMWriterSink::IsRealTime","IWMWriterSinkIsRealTime","IsRealTime","IsRealTime method [windows Media Format]","IsRealTime method [windows Media Format]","IWMWriterSink interface","wmformat.iwmwritersink_isrealtime","wmsdkidl/IWMWriterSink::IsRealTime"]
old-location: wmformat\iwmwritersink_isrealtime.htm
tech.root: wmformat
ms.assetid: 95a32114-4581-4870-8c7f-b79b5af8f0a4
ms.date: 4/26/2023
ms.keywords: IWMWriterSink interface [windows Media Format],IsRealTime method, IWMWriterSink.IsRealTime, IWMWriterSink::IsRealTime, IWMWriterSinkIsRealTime, IsRealTime, IsRealTime method [windows Media Format], IsRealTime method [windows Media Format],IWMWriterSink interface, wmformat.iwmwritersink_isrealtime, wmsdkidl/IWMWriterSink::IsRealTime
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
 - IWMWriterSink::IsRealTime
 - wmsdkidl/IWMWriterSink::IsRealTime
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
 - IWMWriterSink.IsRealTime
---

# IWMWriterSink::IsRealTime


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IsRealTime</b> is called by the writer to determine whether the sink needs data units to be delivered in real time. It is up to you to decide whether your custom sink requires real-time delivery.

## -parameters

### -param pfRealTime [out]

Pointer to a Boolean value that is True if the sink requires real time data unit delivery.

## -returns

This method is implemented by the application. It should always return S_OK.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink Interface</a>