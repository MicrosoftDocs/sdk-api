---
UID: NF:wmsdkidl.IWMStreamPrioritization.SetPriorityRecords
title: IWMStreamPrioritization::SetPriorityRecords (wmsdkidl.h)
description: The SetPriorityRecords method assigns the members of an array as the stream priority list in the stream prioritization object.
helpviewer_keywords: ["IWMStreamPrioritization interface [windows Media Format]","SetPriorityRecords method","IWMStreamPrioritization.SetPriorityRecords","IWMStreamPrioritization::SetPriorityRecords","IWMStreamPrioritizationSetPriorityRecords","SetPriorityRecords","SetPriorityRecords method [windows Media Format]","SetPriorityRecords method [windows Media Format]","IWMStreamPrioritization interface","wmformat.iwmstreamprioritization_setpriorityrecords","wmsdkidl/IWMStreamPrioritization::SetPriorityRecords"]
old-location: wmformat\iwmstreamprioritization_setpriorityrecords.htm
tech.root: wmformat
ms.assetid: 9bd42132-b391-4941-87db-5ce2254e19cf
ms.date: 12/05/2018
ms.keywords: IWMStreamPrioritization interface [windows Media Format],SetPriorityRecords method, IWMStreamPrioritization.SetPriorityRecords, IWMStreamPrioritization::SetPriorityRecords, IWMStreamPrioritizationSetPriorityRecords, SetPriorityRecords, SetPriorityRecords method [windows Media Format], SetPriorityRecords method [windows Media Format],IWMStreamPrioritization interface, wmformat.iwmstreamprioritization_setpriorityrecords, wmsdkidl/IWMStreamPrioritization::SetPriorityRecords
f1_keywords:
- wmsdkidl/IWMStreamPrioritization.SetPriorityRecords
dev_langs:
- c++
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
- IWMStreamPrioritization.SetPriorityRecords
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMStreamPrioritization::SetPriorityRecords


## -description



The <b>SetPriorityRecords</b> method assigns the members of an array as the stream priority list in the stream prioritization object.




## -parameters




### -param pRecordArray [in]

Pointer to an array of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record">WM_STREAM_PRIORITY_RECORD</a> structures.


### -param cRecords [in]

Count of records.


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
<i>cRecords</i> specifies a record count greater than zero, but <i>pRecordArray</i> is <b>NULL</b>.

OR

One of the array rules has been broken (see the Remarks section).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to store the array in the stream prioritization object.

</td>
</tr>
</table>
 




## -remarks



Valid arrays contain no duplicate stream numbers. Streams are listed in the array in descending priority order. Any stream that is designated as mandatory must occur in the array before any entries that are optional. If any of these rules are broken, <b>SetPriorityRecords</b> will return E_INVALIDARG.

<b>SetPriorityRecords</b> overwrites an existing stream priority array if there is one. You can clear the array by passing zero for <i>cRecords</i>.

This method does not verify that the streams specified are valid for the profile.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization">IWMStreamPrioritization Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamprioritization-getpriorityrecords">IWMStreamPrioritization::GetPriorityRecords</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record">WM_STREAM_PRIORITY_RECORD</a>
 

 

