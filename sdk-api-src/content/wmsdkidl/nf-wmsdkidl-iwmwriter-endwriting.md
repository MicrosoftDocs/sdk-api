---
UID: NF:wmsdkidl.IWMWriter.EndWriting
title: IWMWriter::EndWriting (wmsdkidl.h)
description: The EndWriting method performs tasks required at the end of a writing session.
helpviewer_keywords: ["EndWriting","EndWriting method [windows Media Format]","EndWriting method [windows Media Format]","IWMWriter interface","IWMWriter interface [windows Media Format]","EndWriting method","IWMWriter.EndWriting","IWMWriter::EndWriting","IWMWriterEndWriting","wmformat.iwmwriter_endwriting","wmsdkidl/IWMWriter::EndWriting"]
old-location: wmformat\iwmwriter_endwriting.htm
tech.root: wmformat
ms.assetid: 020e2c9d-9581-48c9-bc7b-a0e9e5a60c63
ms.date: 4/26/2023
ms.keywords: EndWriting, EndWriting method [windows Media Format], EndWriting method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],EndWriting method, IWMWriter.EndWriting, IWMWriter::EndWriting, IWMWriterEndWriting, wmformat.iwmwriter_endwriting, wmsdkidl/IWMWriter::EndWriting
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
 - IWMWriter::EndWriting
 - wmsdkidl/IWMWriter::EndWriting
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
 - IWMWriter.EndWriting
---

# IWMWriter::EndWriting


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>EndWriting</b> method performs tasks required at the end of a writing session. This method flushes the buffers, updates indices and headers, and closes the file. You must call <b>EndWriting</b> when you have finished sending samples to the writer to encode an ASF file.



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
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The writer cannot currently be run.

</td>
</tr>
</table>

## -remarks

This method will not return a failure code if the disk space was used up before the encoding was completed. In order to be notified of a file writing error, an application should implement the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a> method and listen for the NS_E_FILE_WRITE event.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a>
