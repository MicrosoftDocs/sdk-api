---
UID: NF:wmsdkidl.IWMWriter.GetInputCount
title: IWMWriter::GetInputCount (wmsdkidl.h)
description: The GetInputCount method retrieves the number of uncompressed input streams.
helpviewer_keywords: ["GetInputCount","GetInputCount method [windows Media Format]","GetInputCount method [windows Media Format]","IWMWriter interface","IWMWriter interface [windows Media Format]","GetInputCount method","IWMWriter.GetInputCount","IWMWriter::GetInputCount","IWMWriterGetInputCount","wmformat.iwmwriter_getinputcount","wmsdkidl/IWMWriter::GetInputCount"]
old-location: wmformat\iwmwriter_getinputcount.htm
tech.root: wmformat
ms.assetid: 0cb3cd79-0640-4a3b-8e8b-d81df2ff749f
ms.date: 4/26/2023
ms.keywords: GetInputCount, GetInputCount method [windows Media Format], GetInputCount method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],GetInputCount method, IWMWriter.GetInputCount, IWMWriter::GetInputCount, IWMWriterGetInputCount, wmformat.iwmwriter_getinputcount, wmsdkidl/IWMWriter::GetInputCount
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
 - IWMWriter::GetInputCount
 - wmsdkidl/IWMWriter::GetInputCount
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
 - IWMWriter.GetInputCount
---

# IWMWriter::GetInputCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetInputCount</b> method retrieves the number of uncompressed input streams.

## -parameters

### -param pcInputs [out]

Pointer to a count of inputs.

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
The <i>pcInputs</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method along with <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops">GetInputProps</a> can be used to enumerate through the various inputs, and get the input format of each. These are not the output Windows Media streams specified in the profile; in a multiple bit rate scenario, one input stream can map to multiple Windows Media streams.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="/windows/desktop/wmformat/to-identify-inputs-by-number">To Identify Inputs By Number</a>