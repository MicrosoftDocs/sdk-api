---
UID: NF:wmsdkidl.IWMMutualExclusion2.RemoveStreamForRecord
title: IWMMutualExclusion2::RemoveStreamForRecord (wmsdkidl.h)
description: The RemoveStreamForRecord method removes a stream from a record's list.
helpviewer_keywords: ["IWMMutualExclusion2 interface [windows Media Format]","RemoveStreamForRecord method","IWMMutualExclusion2.RemoveStreamForRecord","IWMMutualExclusion2::RemoveStreamForRecord","IWMMutualExclusion2RemoveStreamForRecord","RemoveStreamForRecord","RemoveStreamForRecord method [windows Media Format]","RemoveStreamForRecord method [windows Media Format]","IWMMutualExclusion2 interface","wmformat.iwmmutualexclusion2_removestreamforrecord","wmsdkidl/IWMMutualExclusion2::RemoveStreamForRecord"]
old-location: wmformat\iwmmutualexclusion2_removestreamforrecord.htm
tech.root: wmformat
ms.assetid: a32d78b7-47a3-45b6-9575-c290adf86094
ms.date: 4/26/2023
ms.keywords: IWMMutualExclusion2 interface [windows Media Format],RemoveStreamForRecord method, IWMMutualExclusion2.RemoveStreamForRecord, IWMMutualExclusion2::RemoveStreamForRecord, IWMMutualExclusion2RemoveStreamForRecord, RemoveStreamForRecord, RemoveStreamForRecord method [windows Media Format], RemoveStreamForRecord method [windows Media Format],IWMMutualExclusion2 interface, wmformat.iwmmutualexclusion2_removestreamforrecord, wmsdkidl/IWMMutualExclusion2::RemoveStreamForRecord
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
 - IWMMutualExclusion2::RemoveStreamForRecord
 - wmsdkidl/IWMMutualExclusion2::RemoveStreamForRecord
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
 - IWMMutualExclusion2.RemoveStreamForRecord
---

# IWMMutualExclusion2::RemoveStreamForRecord


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>RemoveStreamForRecord</b> method removes a stream from a record's list.

## -parameters

### -param wRecordNumber [in]

<b>WORD</b> containing the record number from which you want to remove a stream.

### -param wStreamNumber [in]

<b>WORD</b> containing the stream number you want to remove from the record.

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
<dt><b>NS_E_NOMATCHING_ELEMENT</b></dt>
</dl>
</td>
<td width="60%">
The stream specified by <i>wStreamNumber</i> does not appear in the record specified by <i>wRecordNumber</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>wRecordNumber</i> does not contain a valid record number.

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

Do not pass <b>NULL</b> for either argument. It will result in exception errors.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2">IWMMutualExclusion2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord">IWMMutualExclusion2::AddStreamForRecord</a>