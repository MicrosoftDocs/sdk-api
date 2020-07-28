---
UID: NF:wmsdkidl.IWMMutualExclusion2.RemoveRecord
title: IWMMutualExclusion2::RemoveRecord (wmsdkidl.h)
description: The RemoveRecord method removes a record from the mutual exclusion object.
helpviewer_keywords: ["IWMMutualExclusion2 interface [windows Media Format]","RemoveRecord method","IWMMutualExclusion2.RemoveRecord","IWMMutualExclusion2::RemoveRecord","IWMMutualExclusion2RemoveRecord","RemoveRecord","RemoveRecord method [windows Media Format]","RemoveRecord method [windows Media Format]","IWMMutualExclusion2 interface","wmformat.iwmmutualexclusion2_removerecord","wmsdkidl/IWMMutualExclusion2::RemoveRecord"]
old-location: wmformat\iwmmutualexclusion2_removerecord.htm
tech.root: wmformat
ms.assetid: 74e2825e-2200-4750-bb16-f8cf9f80ab7e
ms.date: 12/05/2018
ms.keywords: IWMMutualExclusion2 interface [windows Media Format],RemoveRecord method, IWMMutualExclusion2.RemoveRecord, IWMMutualExclusion2::RemoveRecord, IWMMutualExclusion2RemoveRecord, RemoveRecord, RemoveRecord method [windows Media Format], RemoveRecord method [windows Media Format],IWMMutualExclusion2 interface, wmformat.iwmmutualexclusion2_removerecord, wmsdkidl/IWMMutualExclusion2::RemoveRecord
f1_keywords:
- wmsdkidl/IWMMutualExclusion2.RemoveRecord
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
- IWMMutualExclusion2.RemoveRecord
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMMutualExclusion2::RemoveRecord


## -description



The <b>RemoveRecord</b> method removes a record from the mutual exclusion object.




## -parameters




### -param wRecordNumber [in]

<b>WORD</b> containing the number of the record to remove.


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
The <i>wRecordNumber</i> parameter does not contain a valid record number.

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



After you remove a record, it cannot be restored.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2">IWMMutualExclusion2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord">IWMMutualExclusion2::AddRecord</a>
 

 

