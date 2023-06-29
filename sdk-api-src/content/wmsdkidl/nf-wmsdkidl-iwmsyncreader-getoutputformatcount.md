---
UID: NF:wmsdkidl.IWMSyncReader.GetOutputFormatCount
title: IWMSyncReader::GetOutputFormatCount (wmsdkidl.h)
description: The GetOutputFormatCount method is used to determine all possible format types supported by this output on the synchronous reader.
helpviewer_keywords: ["GetOutputFormatCount","GetOutputFormatCount method [windows Media Format]","GetOutputFormatCount method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","GetOutputFormatCount method","IWMSyncReader.GetOutputFormatCount","IWMSyncReader::GetOutputFormatCount","IWMSyncReaderGetOutputFormatCount","wmformat.iwmsyncreader_getoutputformatcount","wmsdkidl/IWMSyncReader::GetOutputFormatCount"]
old-location: wmformat\iwmsyncreader_getoutputformatcount.htm
tech.root: wmformat
ms.assetid: 66f66784-791b-4f1b-8ba2-300a4521ce03
ms.date: 4/26/2023
ms.keywords: GetOutputFormatCount, GetOutputFormatCount method [windows Media Format], GetOutputFormatCount method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetOutputFormatCount method, IWMSyncReader.GetOutputFormatCount, IWMSyncReader::GetOutputFormatCount, IWMSyncReaderGetOutputFormatCount, wmformat.iwmsyncreader_getoutputformatcount, wmsdkidl/IWMSyncReader::GetOutputFormatCount
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
 - IWMSyncReader::GetOutputFormatCount
 - wmsdkidl/IWMSyncReader::GetOutputFormatCount
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
 - IWMSyncReader.GetOutputFormatCount
---

# IWMSyncReader::GetOutputFormatCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetOutputFormatCount</b> method is used to determine all possible format types supported by this output on the synchronous reader.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> containing the output number for which you want to determine the number of supported formats.

### -param pcFormats [out]

Pointer to a <b>DWORD</b> that receives the number of supported formats.

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
<i>pcFormats</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
There is no file loaded in the synchronous reader.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat">IWMSyncReader::GetOutputFormat</a>