---
UID: NF:wmsdkidl.IWMMutualExclusion2.AddRecord
title: IWMMutualExclusion2::AddRecord (wmsdkidl.h)
description: The AddRecord method adds a record to the mutual exclusion object.
helpviewer_keywords: ["AddRecord","AddRecord method [windows Media Format]","AddRecord method [windows Media Format]","IWMMutualExclusion2 interface","IWMMutualExclusion2 interface [windows Media Format]","AddRecord method","IWMMutualExclusion2.AddRecord","IWMMutualExclusion2::AddRecord","IWMMutualExclusion2AddRecord","wmformat.iwmmutualexclusion2_addrecord","wmsdkidl/IWMMutualExclusion2::AddRecord"]
old-location: wmformat\iwmmutualexclusion2_addrecord.htm
tech.root: wmformat
ms.assetid: 58eaa4b2-65d3-44b1-8e3d-1aac01057d0f
ms.date: 12/05/2018
ms.keywords: AddRecord, AddRecord method [windows Media Format], AddRecord method [windows Media Format],IWMMutualExclusion2 interface, IWMMutualExclusion2 interface [windows Media Format],AddRecord method, IWMMutualExclusion2.AddRecord, IWMMutualExclusion2::AddRecord, IWMMutualExclusion2AddRecord, wmformat.iwmmutualexclusion2_addrecord, wmsdkidl/IWMMutualExclusion2::AddRecord
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
 - IWMMutualExclusion2::AddRecord
 - wmsdkidl/IWMMutualExclusion2::AddRecord
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
 - IWMMutualExclusion2.AddRecord
---

# IWMMutualExclusion2::AddRecord


## -description

The <b>AddRecord</b> method adds a record to the mutual exclusion object. Records can hold groups of streams. You can add streams with calls to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord">IWMMutualExclusion2::AddStreamForRecord</a>. You can assign a name to a record with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-setname">IWMMutualExclusion2::SetName</a>.



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
The method was unable to allocate memory for the new record.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was a problem adding the new record to the collection of records for this mutual exclusion object.

</td>
</tr>
</table>

## -remarks

Record numbers, which are used by other methods, are assigned to records sequentially.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2">IWMMutualExclusion2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord">IWMMutualExclusion2::AddStreamForRecord</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-removerecord">IWMMutualExclusion2::RemoveRecord</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-setname">IWMMutualExclusion2::SetName</a>
