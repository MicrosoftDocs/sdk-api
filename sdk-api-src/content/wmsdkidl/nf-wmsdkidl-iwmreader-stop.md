---
UID: NF:wmsdkidl.IWMReader.Stop
title: IWMReader::Stop (wmsdkidl.h)
description: The Stop method stops reading the file.
helpviewer_keywords: ["IWMReader interface [windows Media Format]","Stop method","IWMReader.Stop","IWMReader::Stop","IWMReaderStop","Stop","Stop method [windows Media Format]","Stop method [windows Media Format]","IWMReader interface","wmformat.iwmreader_stop","wmsdkidl/IWMReader::Stop"]
old-location: wmformat\iwmreader_stop.htm
tech.root: wmformat
ms.assetid: 781d1882-4b48-4415-9b3a-788207b42151
ms.date: 4/26/2023
ms.keywords: IWMReader interface [windows Media Format],Stop method, IWMReader.Stop, IWMReader::Stop, IWMReaderStop, Stop, Stop method [windows Media Format], Stop method [windows Media Format],IWMReader interface, wmformat.iwmreader_stop, wmsdkidl/IWMReader::Stop
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
 - IWMReader::Stop
 - wmsdkidl/IWMReader::Stop
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
 - IWMReader.Stop
---

# IWMReader::Stop


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Stop</b> method stops reading the file.



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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

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
</table>

## -remarks

This method sends a WMT_STOPPED status notification to the application's <b>IWMReaderCallback::OnStatus</b> function.

Calling <b>Stop</b> eliminates the current read position. If <b>Start</b> is called with a start time set at WM_START_CURRENTPOSITION after calling <b>Stop</b>, an error is returned.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-close">IWMReader::Close</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">IWMReader::Open</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">IWMReader::Start</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback Interface</a>
