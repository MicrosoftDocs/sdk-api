---
UID: NF:wmsdkidl.IWMReaderAdvanced2.StopBuffering
title: IWMReaderAdvanced2::StopBuffering (wmsdkidl.h)
description: The StopBuffering method requests that the reader send the WMT_BUFFERING_STOP message as soon as possible.
helpviewer_keywords: ["IWMReaderAdvanced2 interface [windows Media Format]","StopBuffering method","IWMReaderAdvanced2.StopBuffering","IWMReaderAdvanced2::StopBuffering","IWMReaderAdvanced2StopBuffering","StopBuffering","StopBuffering method [windows Media Format]","StopBuffering method [windows Media Format]","IWMReaderAdvanced2 interface","wmformat.iwmreaderadvanced2_stopbuffering","wmsdkidl/IWMReaderAdvanced2::StopBuffering"]
old-location: wmformat\iwmreaderadvanced2_stopbuffering.htm
tech.root: wmformat
ms.assetid: 3c380a68-d86c-421a-8102-019848893c35
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced2 interface [windows Media Format],StopBuffering method, IWMReaderAdvanced2.StopBuffering, IWMReaderAdvanced2::StopBuffering, IWMReaderAdvanced2StopBuffering, StopBuffering, StopBuffering method [windows Media Format], StopBuffering method [windows Media Format],IWMReaderAdvanced2 interface, wmformat.iwmreaderadvanced2_stopbuffering, wmsdkidl/IWMReaderAdvanced2::StopBuffering
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
 - IWMReaderAdvanced2::StopBuffering
 - wmsdkidl/IWMReaderAdvanced2::StopBuffering
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
 - IWMReaderAdvanced2.StopBuffering
---

# IWMReaderAdvanced2::StopBuffering


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>StopBuffering</b> method requests that the reader send the WMT_BUFFERING_STOP message as soon as possible.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The reader responds to the request to stop buffering only if it is currently buffering data. This means it has sent a WMT_BUFFERING_START message, but not sent the corresponding WMT_BUFFERING_STOP. There is, however, no guarantee of how quickly the reader responds to the request. This feature is particularly useful when the play mode is set to WMT_PLAY_MODE_DOWNLOAD.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_play_mode">WMT_PLAY_MODE</a>
