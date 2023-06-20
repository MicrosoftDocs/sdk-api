---
UID: NF:wmsdkidl.IWMReader.GetOutputCount
title: IWMReader::GetOutputCount (wmsdkidl.h)
description: The GetOutputCount method retrieves the number of uncompressed media streams that will be delivered for the file loaded in the reader.
helpviewer_keywords: ["GetOutputCount","GetOutputCount method [windows Media Format]","GetOutputCount method [windows Media Format]","IWMReader interface","IWMReader interface [windows Media Format]","GetOutputCount method","IWMReader.GetOutputCount","IWMReader::GetOutputCount","IWMReaderGetOutputCount","wmformat.iwmreader_getoutputcount","wmsdkidl/IWMReader::GetOutputCount"]
old-location: wmformat\iwmreader_getoutputcount.htm
tech.root: wmformat
ms.assetid: 4f04fad9-a638-45c6-b924-50f57472dfe3
ms.date: 4/26/2023
ms.keywords: GetOutputCount, GetOutputCount method [windows Media Format], GetOutputCount method [windows Media Format],IWMReader interface, IWMReader interface [windows Media Format],GetOutputCount method, IWMReader.GetOutputCount, IWMReader::GetOutputCount, IWMReaderGetOutputCount, wmformat.iwmreader_getoutputcount, wmsdkidl/IWMReader::GetOutputCount
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
 - IWMReader::GetOutputCount
 - wmsdkidl/IWMReader::GetOutputCount
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
 - IWMReader.GetOutputCount
---

# IWMReader::GetOutputCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetOutputCount</b> method retrieves the number of uncompressed media streams that will be delivered for the file loaded in the reader.

## -parameters

### -param pcOutputs [out]

Pointer to a count of outputs.

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
The <i>pcOutputs</i> parameter is <b>NULL</b>.

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

A file with mutually exclusive streams contains several streams that are delivered to the same output. But only one of those streams can be delivered at a time during playback. When reading a file, you can identify its outputs by looping through the outputs and getting the media properties of each by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops">IWMReader::GetOutputProps</a>.

This method is synchronous and does not result in any messages being sent to the status callback.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops">IWMReader::GetOutputProps</a>