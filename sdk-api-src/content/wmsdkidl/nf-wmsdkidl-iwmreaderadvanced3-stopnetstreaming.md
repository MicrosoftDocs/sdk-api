---
UID: NF:wmsdkidl.IWMReaderAdvanced3.StopNetStreaming
title: IWMReaderAdvanced3::StopNetStreaming (wmsdkidl.h)
description: The StopNetStreaming method halts network streaming. Any samples that have already been received from the network are delivered as usual.
helpviewer_keywords: ["IWMReaderAdvanced3 interface [windows Media Format]","StopNetStreaming method","IWMReaderAdvanced3.StopNetStreaming","IWMReaderAdvanced3::StopNetStreaming","IWMReaderAdvanced3StopNetStreaming","StopNetStreaming","StopNetStreaming method [windows Media Format]","StopNetStreaming method [windows Media Format]","IWMReaderAdvanced3 interface","wmformat.iwmreaderadvanced3_stopnetstreaming","wmsdkidl/IWMReaderAdvanced3::StopNetStreaming"]
old-location: wmformat\iwmreaderadvanced3_stopnetstreaming.htm
tech.root: wmformat
ms.assetid: e323f967-02d5-4472-a9b3-cb8a2b80070e
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced3 interface [windows Media Format],StopNetStreaming method, IWMReaderAdvanced3.StopNetStreaming, IWMReaderAdvanced3::StopNetStreaming, IWMReaderAdvanced3StopNetStreaming, StopNetStreaming, StopNetStreaming method [windows Media Format], StopNetStreaming method [windows Media Format],IWMReaderAdvanced3 interface, wmformat.iwmreaderadvanced3_stopnetstreaming, wmsdkidl/IWMReaderAdvanced3::StopNetStreaming
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
 - IWMReaderAdvanced3::StopNetStreaming
 - wmsdkidl/IWMReaderAdvanced3::StopNetStreaming
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
 - IWMReaderAdvanced3.StopNetStreaming
---

# IWMReaderAdvanced3::StopNetStreaming


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>StopNetStreaming</b> method halts network streaming. Any samples that have already been received from the network are delivered as usual.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

When this method is finished, a WMT_END_OF_STREAMING message will be delivered to the <b>OnStatus</b> method.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3">IWMReaderAdvanced3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a>
