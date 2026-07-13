---
UID: NF:wmsdkidl.IWMSyncReader.GetOutputFormat
title: IWMSyncReader::GetOutputFormat (wmsdkidl.h)
description: The GetOutputFormat method retrieves the supported formats for a specified output media stream.
helpviewer_keywords: ["GetOutputFormat","GetOutputFormat method [windows Media Format]","GetOutputFormat method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","GetOutputFormat method","IWMSyncReader.GetOutputFormat","IWMSyncReader::GetOutputFormat","IWMSyncReaderGetOutputFormat","wmformat.iwmsyncreader_getoutputformat","wmsdkidl/IWMSyncReader::GetOutputFormat"]
old-location: wmformat\iwmsyncreader_getoutputformat.htm
tech.root: wmformat
ms.assetid: 7faac9e7-ad5f-42a4-ba6e-562ae973f81b
ms.date: 4/26/2023
ms.keywords: GetOutputFormat, GetOutputFormat method [windows Media Format], GetOutputFormat method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetOutputFormat method, IWMSyncReader.GetOutputFormat, IWMSyncReader::GetOutputFormat, IWMSyncReaderGetOutputFormat, wmformat.iwmsyncreader_getoutputformat, wmsdkidl/IWMSyncReader::GetOutputFormat
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
 - IWMSyncReader::GetOutputFormat
 - wmsdkidl/IWMSyncReader::GetOutputFormat
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
 - IWMSyncReader.GetOutputFormat
---

# IWMSyncReader::GetOutputFormat


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetOutputFormat</b> method retrieves the supported formats for a specified output media stream.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.

### -param dwFormatNum [in]

<b>DWORD</b> containing the format number.

### -param ppProps [out]

Pointer to a pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps</a> interface. This object is created by a successful call to this method.

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
<i>ppProps</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
No file is open in the synchronous reader.

</td>
</tr>
</table>

## -remarks

To enumerate the supported formats for an output media stream, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount">GetOutputFormatCount</a> to get the number of formats, and then call <b>GetOutputFormat</b> in succession to get the formats.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>