---
UID: NF:wmsdkidl.IWMWriterFileSink.Open
title: IWMWriterFileSink::Open (wmsdkidl.h)
description: The Open method opens a file that acts as the writer sink.
helpviewer_keywords: ["IWMWriterFileSink interface [windows Media Format]","Open method","IWMWriterFileSink.Open","IWMWriterFileSink::Open","IWMWriterFileSinkOpen","Open","Open method [windows Media Format]","Open method [windows Media Format]","IWMWriterFileSink interface","wmformat.iwmwriterfilesink_open","wmsdkidl/IWMWriterFileSink::Open"]
old-location: wmformat\iwmwriterfilesink_open.htm
tech.root: wmformat
ms.assetid: 14a36fe9-8293-4079-8189-8a8e0720c100
ms.date: 12/05/2018
ms.keywords: IWMWriterFileSink interface [windows Media Format],Open method, IWMWriterFileSink.Open, IWMWriterFileSink::Open, IWMWriterFileSinkOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMWriterFileSink interface, wmformat.iwmwriterfilesink_open, wmsdkidl/IWMWriterFileSink::Open
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
 - IWMWriterFileSink::Open
 - wmsdkidl/IWMWriterFileSink::Open
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
 - IWMWriterFileSink.Open
---

# IWMWriterFileSink::Open


## -description

The <b>Open</b> method opens a file that acts as the writer sink.

## -parameters

### -param pwszFilename [in]

Pointer to a wide-character <b>null</b>-terminated string containing the file name. URLs are not supported.

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
The <i>pwszFilename</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

There is no close method in this interface as the closing of the writer sink file is done automatically by a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting">IWMWriter::EndWriting</a>.

See the Remarks and Example Code sections for <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink">IWMWriterFileSink Interface</a>