---
UID: NF:wmsdkidl.IWMSyncReader.GetOutputProps
title: IWMSyncReader::GetOutputProps (wmsdkidl.h)
description: The GetOutputProps method retrieves the current properties of an uncompressed output stream.
helpviewer_keywords: ["GetOutputProps","GetOutputProps method [windows Media Format]","GetOutputProps method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","GetOutputProps method","IWMSyncReader.GetOutputProps","IWMSyncReader::GetOutputProps","IWMSyncReaderGetOutputProps","wmformat.iwmsyncreader_getoutputprops","wmsdkidl/IWMSyncReader::GetOutputProps"]
old-location: wmformat\iwmsyncreader_getoutputprops.htm
tech.root: wmformat
ms.assetid: a5e701ea-8b53-4abe-8b78-7c6fb151d80f
ms.date: 4/26/2023
ms.keywords: GetOutputProps, GetOutputProps method [windows Media Format], GetOutputProps method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetOutputProps method, IWMSyncReader.GetOutputProps, IWMSyncReader::GetOutputProps, IWMSyncReaderGetOutputProps, wmformat.iwmsyncreader_getoutputprops, wmsdkidl/IWMSyncReader::GetOutputProps
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
 - IWMSyncReader::GetOutputProps
 - wmsdkidl/IWMSyncReader::GetOutputProps
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
 - IWMSyncReader.GetOutputProps
---

# IWMSyncReader::GetOutputProps


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetOutputProps</b> method retrieves the current properties of an uncompressed output stream.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.

### -param ppOutput [out]

Pointer to a pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps</a> interface, which is created by a successful call to this method.

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
The <i>ppOutput</i> parameter is <b>NULL</b>, or the <i>dwOutputNum</i> parameter is greater than or equal to the number of outputs. Output numbers begin with zero.

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

Manipulating the object retrieved by a call to <b>GetOutputProps</b> has no effect on the output media stream, unless the application also calls <b>SetOutputProps</b>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops">IWMSyncReader::SetOutputProps</a>