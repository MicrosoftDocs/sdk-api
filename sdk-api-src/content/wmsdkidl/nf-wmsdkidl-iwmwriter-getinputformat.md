---
UID: NF:wmsdkidl.IWMWriter.GetInputFormat
title: IWMWriter::GetInputFormat (wmsdkidl.h)
description: The GetInputFormat method retrieves possible media formats for the specified input.
helpviewer_keywords: ["GetInputFormat","GetInputFormat method [windows Media Format]","GetInputFormat method [windows Media Format]","IWMWriter interface","IWMWriter interface [windows Media Format]","GetInputFormat method","IWMWriter.GetInputFormat","IWMWriter::GetInputFormat","IWMWriterGetInputFormat","wmformat.iwmwriter_getinputformat","wmsdkidl/IWMWriter::GetInputFormat"]
old-location: wmformat\iwmwriter_getinputformat.htm
tech.root: wmformat
ms.assetid: c058de81-a29a-4bcd-a819-3cdef11cae9f
ms.date: 4/26/2023
ms.keywords: GetInputFormat, GetInputFormat method [windows Media Format], GetInputFormat method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],GetInputFormat method, IWMWriter.GetInputFormat, IWMWriter::GetInputFormat, IWMWriterGetInputFormat, wmformat.iwmwriter_getinputformat, wmsdkidl/IWMWriter::GetInputFormat
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
 - IWMWriter::GetInputFormat
 - wmsdkidl/IWMWriter::GetInputFormat
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
 - IWMWriter.GetInputFormat
---

# IWMWriter::GetInputFormat


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetInputFormat</b> method retrieves possible media formats for the specified input.

## -parameters

### -param dwInputNumber [in]

<b>DWORD</b> containing the input number.

### -param dwFormatNumber [in]

<b>DWORD</b> containing the format number.

### -param pProps [out]

Pointer to a pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops">IWMInputMediaProps</a> interface.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwInputNumber</i> is too large.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount">IWMWriter::GetInputFormatCount</a>



<a href="/windows/desktop/wmformat/to-enumerate-input-formats">To Enumerate Input Formats</a>