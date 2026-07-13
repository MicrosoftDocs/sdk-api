---
UID: NF:wmsdkidl.IWMReaderAdvanced2.Preroll
title: IWMReaderAdvanced2::Preroll (wmsdkidl.h)
description: The Preroll method is used to begin prerolling (buffering data) for the reader.
helpviewer_keywords: ["IWMReaderAdvanced2 interface [windows Media Format]","Preroll method","IWMReaderAdvanced2.Preroll","IWMReaderAdvanced2::Preroll","IWMReaderAdvanced2Preroll","Preroll","Preroll method [windows Media Format]","Preroll method [windows Media Format]","IWMReaderAdvanced2 interface","wmformat.iwmreaderadvanced2_preroll","wmsdkidl/IWMReaderAdvanced2::Preroll"]
old-location: wmformat\iwmreaderadvanced2_preroll.htm
tech.root: wmformat
ms.assetid: c216adf1-390c-45cc-acae-645fe29f55de
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced2 interface [windows Media Format],Preroll method, IWMReaderAdvanced2.Preroll, IWMReaderAdvanced2::Preroll, IWMReaderAdvanced2Preroll, Preroll, Preroll method [windows Media Format], Preroll method [windows Media Format],IWMReaderAdvanced2 interface, wmformat.iwmreaderadvanced2_preroll, wmsdkidl/IWMReaderAdvanced2::Preroll
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
 - IWMReaderAdvanced2::Preroll
 - wmsdkidl/IWMReaderAdvanced2::Preroll
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
 - IWMReaderAdvanced2.Preroll
---

# IWMReaderAdvanced2::Preroll


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Preroll</b> method is used to begin prerolling (buffering data) for the reader.

## -parameters

### -param cnsStart [in]

Specifies the start time in 100-nanosecond units.

### -param cnsDuration [in]

Specifies the duration in 100-nanosecond units.

### -param fRate [in]

Specifies the data rate.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be called before the application calls <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">Start</a> to begin buffering data in advance. The parameters here must be set to the same values as those that are passed to <b>Start</b> when it is called. If the parameters are different, <b>Start</b> will do rebuffering.

It is important to allow sufficient time for the prerolling (buffering data) for the reader to be completed before calling <b>Start</b>. When prerolling local files, 6 seconds normally is sufficient. When prerolling files over the Internet, allow more time before calling <b>Start</b>. If insufficient time is allowed, the effect will be a longer <b>Start</b> time when <b>Start</b> is called.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>