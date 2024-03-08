---
UID: NF:wmsdkidl.IWMWriterFileSink2.Stop
title: IWMWriterFileSink2::Stop (wmsdkidl.h)
description: The Stop method stops recording at the specified time.
helpviewer_keywords: ["IWMWriterFileSink2 interface [windows Media Format]","Stop method","IWMWriterFileSink2.Stop","IWMWriterFileSink2::Stop","IWMWriterFileSink2Stop","Stop","Stop method [windows Media Format]","Stop method [windows Media Format]","IWMWriterFileSink2 interface","wmformat.iwmwriterfilesink2_stop","wmsdkidl/IWMWriterFileSink2::Stop"]
old-location: wmformat\iwmwriterfilesink2_stop.htm
tech.root: wmformat
ms.assetid: 47377c77-f534-4bb0-be57-49bdb109c309
ms.date: 4/26/2023
ms.keywords: IWMWriterFileSink2 interface [windows Media Format],Stop method, IWMWriterFileSink2.Stop, IWMWriterFileSink2::Stop, IWMWriterFileSink2Stop, Stop, Stop method [windows Media Format], Stop method [windows Media Format],IWMWriterFileSink2 interface, wmformat.iwmwriterfilesink2_stop, wmsdkidl/IWMWriterFileSink2::Stop
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
 - IWMWriterFileSink2::Stop
 - wmsdkidl/IWMWriterFileSink2::Stop
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
 - IWMWriterFileSink2.Stop
---

# IWMWriterFileSink2::Stop


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Stop</b> method stops recording at the specified time.

## -parameters

### -param cnsStopTime [in]

Stop time in 100-nanosecond units.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

Because of interleaving of streams with slightly different time stamps at any particular point in the file, the actual stop time might not be exactly as specified in <i>cnsStopTime</i>. To increase the precision, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setcontrolstream">IWMWriterFileSink3::SetControlStream</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close">IWMWriterFileSink2::Close</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start">IWMWriterFileSink2::Start</a>