---
UID: NF:wmsdkidl.IWMWriterFileSink3.GetUnbufferedIO
title: IWMWriterFileSink3::GetUnbufferedIO (wmsdkidl.h)
description: The GetUnbufferedIO method ascertains whether unbuffered I/O is used for the file sink.
helpviewer_keywords: ["GetUnbufferedIO","GetUnbufferedIO method [windows Media Format]","GetUnbufferedIO method [windows Media Format]","IWMWriterFileSink3 interface","IWMWriterFileSink3 interface [windows Media Format]","GetUnbufferedIO method","IWMWriterFileSink3.GetUnbufferedIO","IWMWriterFileSink3::GetUnbufferedIO","IWMWriterFileSink3GetUnbufferedIO","wmformat.iwmwriterfilesink3_getunbufferedio","wmsdkidl/IWMWriterFileSink3::GetUnbufferedIO"]
old-location: wmformat\iwmwriterfilesink3_getunbufferedio.htm
tech.root: wmformat
ms.assetid: e87222eb-6ed1-49b7-a544-27703ba9806b
ms.date: 4/26/2023
ms.keywords: GetUnbufferedIO, GetUnbufferedIO method [windows Media Format], GetUnbufferedIO method [windows Media Format],IWMWriterFileSink3 interface, IWMWriterFileSink3 interface [windows Media Format],GetUnbufferedIO method, IWMWriterFileSink3.GetUnbufferedIO, IWMWriterFileSink3::GetUnbufferedIO, IWMWriterFileSink3GetUnbufferedIO, wmformat.iwmwriterfilesink3_getunbufferedio, wmsdkidl/IWMWriterFileSink3::GetUnbufferedIO
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
 - IWMWriterFileSink3::GetUnbufferedIO
 - wmsdkidl/IWMWriterFileSink3::GetUnbufferedIO
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
 - IWMWriterFileSink3.GetUnbufferedIO
---

# IWMWriterFileSink3::GetUnbufferedIO


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetUnbufferedIO</b> method ascertains whether unbuffered I/O is used for the file sink.

## -parameters

### -param pfUnbufferedIO [out]

Pointer to a Boolean value that is set to True if unbuffered I/O is used with this file sink.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pfUnbuffered</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3">IWMWriterFileSink3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setunbufferedio">IWMWriterFileSink3::SetUnbufferedIO</a>