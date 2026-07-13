---
UID: NF:wmsdkidl.IWMMutualExclusion2.AddStreamForRecord
title: IWMMutualExclusion2::AddStreamForRecord (wmsdkidl.h)
description: The AddStreamForRecord method adds a stream to a record created with IWMMutualExclusion2::AddRecord.
helpviewer_keywords: ["AddStreamForRecord","AddStreamForRecord method [windows Media Format]","AddStreamForRecord method [windows Media Format]","IWMMutualExclusion2 interface","IWMMutualExclusion2 interface [windows Media Format]","AddStreamForRecord method","IWMMutualExclusion2.AddStreamForRecord","IWMMutualExclusion2::AddStreamForRecord","IWMMutualExclusion2AddStreamForRecord","wmformat.iwmmutualexclusion2_addstreamforrecord","wmsdkidl/IWMMutualExclusion2::AddStreamForRecord"]
old-location: wmformat\iwmmutualexclusion2_addstreamforrecord.htm
tech.root: wmformat
ms.assetid: 501fae9f-84b3-4025-83bc-ad0bbe47384d
ms.date: 4/26/2023
ms.keywords: AddStreamForRecord, AddStreamForRecord method [windows Media Format], AddStreamForRecord method [windows Media Format],IWMMutualExclusion2 interface, IWMMutualExclusion2 interface [windows Media Format],AddStreamForRecord method, IWMMutualExclusion2.AddStreamForRecord, IWMMutualExclusion2::AddStreamForRecord, IWMMutualExclusion2AddStreamForRecord, wmformat.iwmmutualexclusion2_addstreamforrecord, wmsdkidl/IWMMutualExclusion2::AddStreamForRecord
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
 - IWMMutualExclusion2::AddStreamForRecord
 - wmsdkidl/IWMMutualExclusion2::AddStreamForRecord
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
 - IWMMutualExclusion2.AddStreamForRecord
---

# IWMMutualExclusion2::AddStreamForRecord


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddStreamForRecord</b> method adds a stream to a record created with <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord">IWMMutualExclusion2::AddRecord</a>.

## -parameters

### -param wRecordNumber [in]

<b>WORD</b> containing the number of the record to which to add the stream.

### -param wStreamNumber [in]

<b>WORD</b> containing the stream number you want to add.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory for the new stream number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>wRecordNumber</i> contains an invalid record number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to access the record for an unspecified reason.

</td>
</tr>
</table>

## -remarks

Record numbers are assigned sequentially.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2">IWMMutualExclusion2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-removestreamforrecord">IWMMutualExclusion2::RemoveStreamForRecord</a>