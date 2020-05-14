---
UID: NF:wmsdkidl.IWMProfile.GetMutualExclusion
title: IWMProfile::GetMutualExclusion (wmsdkidl.h)
description: The GetMutualExclusion method retrieves a mutual exclusion object from the profile.helpviewer_keywords: ["GetMutualExclusion","GetMutualExclusion method [windows Media Format]","GetMutualExclusion method [windows Media Format]","IWMProfile interface","GetMutualExclusion method [windows Media Format]","IWMProfile2 interface","GetMutualExclusion method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","GetMutualExclusion method","IWMProfile.GetMutualExclusion","IWMProfile2 interface [windows Media Format]","GetMutualExclusion method","IWMProfile2::GetMutualExclusion","IWMProfile3 interface [windows Media Format]","GetMutualExclusion method","IWMProfile3::GetMutualExclusion","IWMProfile::GetMutualExclusion","IWMProfileGetMutualExclusion","wmformat.iwmprofile_getmutualexclusion","wmsdkidl/IWMProfile2::GetMutualExclusion","wmsdkidl/IWMProfile3::GetMutualExclusion","wmsdkidl/IWMProfile::GetMutualExclusion"]
old-location: wmformat\iwmprofile_getmutualexclusion.htm
tech.root: wmformat
ms.assetid: 949bb57f-8656-420e-b317-8ca7eb977a4e
ms.date: 12/05/2018
ms.keywords: GetMutualExclusion, GetMutualExclusion method [windows Media Format], GetMutualExclusion method [windows Media Format],IWMProfile interface, GetMutualExclusion method [windows Media Format],IWMProfile2 interface, GetMutualExclusion method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetMutualExclusion method, IWMProfile.GetMutualExclusion, IWMProfile2 interface [windows Media Format],GetMutualExclusion method, IWMProfile2::GetMutualExclusion, IWMProfile3 interface [windows Media Format],GetMutualExclusion method, IWMProfile3::GetMutualExclusion, IWMProfile::GetMutualExclusion, IWMProfileGetMutualExclusion, wmformat.iwmprofile_getmutualexclusion, wmsdkidl/IWMProfile2::GetMutualExclusion, wmsdkidl/IWMProfile3::GetMutualExclusion, wmsdkidl/IWMProfile::GetMutualExclusion
f1_keywords:
- wmsdkidl/IWMProfile.GetMutualExclusion
dev_langs:
- c++
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
- qasf.dll
api_name:
- IWMProfile.GetMutualExclusion
- IWMProfile2.GetMutualExclusion
- IWMProfile3.GetMutualExclusion
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile::GetMutualExclusion


## -description



The <b>GetMutualExclusion</b> method retrieves a mutual exclusion object from the profile.




## -parameters




### -param dwMEIndex [in]

<b>DWORD</b> containing the index of the mutual exclusion object.


### -param ppME [out]

Pointer to a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion">IWMMutualExclusion</a> interface of the mutual exclusion object specified by the index passed as <i>dwMEIndex</i>.


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
Not enough memory for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppME</i> is <b>NULL</b>, or <i>dwMEIndex</i> is outside the range of indexes available.

</td>
</tr>
</table>
 




## -remarks



You can use this method in conjunction with <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusioncount">GetMutualExclusionCount</a> to step through all of the mutual exclusion objects in the profile.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion">IWMProfile::AddMutualExclusion</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion">IWMProfile::RemoveMutualExclusion</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/mutual-exclusion">Mutual Exclusion</a>
 

 

