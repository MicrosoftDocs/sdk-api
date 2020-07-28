---
UID: NF:wmsdkidl.IWMMutualExclusion2.GetRecordCount
title: IWMMutualExclusion2::GetRecordCount (wmsdkidl.h)
description: The GetRecordCount method retrieves the number of records present in the mutual exclusion object.
helpviewer_keywords: ["GetRecordCount","GetRecordCount method [windows Media Format]","GetRecordCount method [windows Media Format]","IWMMutualExclusion2 interface","IWMMutualExclusion2 interface [windows Media Format]","GetRecordCount method","IWMMutualExclusion2.GetRecordCount","IWMMutualExclusion2::GetRecordCount","IWMMutualExclusion2GetRecordCount","wmformat.iwmmutualexclusion2_getrecordcount","wmsdkidl/IWMMutualExclusion2::GetRecordCount"]
old-location: wmformat\iwmmutualexclusion2_getrecordcount.htm
tech.root: wmformat
ms.assetid: 6e113601-1ac7-42a3-8e46-f1ba67ebb071
ms.date: 12/05/2018
ms.keywords: GetRecordCount, GetRecordCount method [windows Media Format], GetRecordCount method [windows Media Format],IWMMutualExclusion2 interface, IWMMutualExclusion2 interface [windows Media Format],GetRecordCount method, IWMMutualExclusion2.GetRecordCount, IWMMutualExclusion2::GetRecordCount, IWMMutualExclusion2GetRecordCount, wmformat.iwmmutualexclusion2_getrecordcount, wmsdkidl/IWMMutualExclusion2::GetRecordCount
f1_keywords:
- wmsdkidl/IWMMutualExclusion2.GetRecordCount
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
- IWMMutualExclusion2.GetRecordCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMMutualExclusion2::GetRecordCount


## -description



The <b>GetRecordCount</b> method retrieves the number of records present in the mutual exclusion object.




## -parameters




### -param pwRecordCount [out]

Pointer to a <b>WORD</b> containing the number of records that exist in the mutual exclusion object.


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
The <i>pwRecordCount</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Record numbers are assigned sequentially.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2">IWMMutualExclusion2 Interface</a>
 

 

