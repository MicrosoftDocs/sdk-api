---
UID: NF:wmsdkidl.IWMWriter.GetInputFormatCount
title: IWMWriter::GetInputFormatCount (wmsdkidl.h)
description: The GetInputFormatCount method retrieves the number of media format types supported by this input on the writer.
helpviewer_keywords: ["GetInputFormatCount","GetInputFormatCount method [windows Media Format]","GetInputFormatCount method [windows Media Format]","IWMWriter interface","IWMWriter interface [windows Media Format]","GetInputFormatCount method","IWMWriter.GetInputFormatCount","IWMWriter::GetInputFormatCount","IWMWriterGetInputFormatCount","wmformat.iwmwriter_getinputformatcount","wmsdkidl/IWMWriter::GetInputFormatCount"]
old-location: wmformat\iwmwriter_getinputformatcount.htm
tech.root: wmformat
ms.assetid: c3afe9e8-e045-4329-b3e5-6026147322ad
ms.date: 12/05/2018
ms.keywords: GetInputFormatCount, GetInputFormatCount method [windows Media Format], GetInputFormatCount method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],GetInputFormatCount method, IWMWriter.GetInputFormatCount, IWMWriter::GetInputFormatCount, IWMWriterGetInputFormatCount, wmformat.iwmwriter_getinputformatcount, wmsdkidl/IWMWriter::GetInputFormatCount
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
 - IWMWriter::GetInputFormatCount
 - wmsdkidl/IWMWriter::GetInputFormatCount
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
 - IWMWriter.GetInputFormatCount
---

# IWMWriter::GetInputFormatCount


## -description

The <b>GetInputFormatCount</b> method retrieves the number of media format types supported by this input on the writer.

## -parameters

### -param dwInputNumber [in]

<b>DWORD</b> containing the input number.

### -param pcFormats [out]

Pointer to a count of formats.

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
The <i>pcFormats</i> parameter is <b>NULL</b>.

OR

<i>dwInputNumber</i> is too large.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat">IWMWriter::GetInputFormat</a>



<a href="/windows/desktop/wmformat/to-enumerate-input-formats">To Enumerate Input Formats</a>