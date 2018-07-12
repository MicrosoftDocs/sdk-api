---
UID: NF:wmsdkidl.IWMProfile.AddMutualExclusion
title: IWMProfile::AddMutualExclusion
author: windows-sdk-content
description: The AddMutualExclusion method adds a mutual exclusion object to the profile. Mutual exclusion objects are used to specify a set of streams, only one of which can be output at a time.
old-location: wmformat\iwmprofile_addmutualexclusion.htm
old-project: wmformat
ms.assetid: efd751cf-d34d-4e74-9a00-444ec31ebef0
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: AddMutualExclusion, AddMutualExclusion method [windows Media Format], AddMutualExclusion method [windows Media Format],IWMProfile interface, AddMutualExclusion method [windows Media Format],IWMProfile2 interface, AddMutualExclusion method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],AddMutualExclusion method, IWMProfile.AddMutualExclusion, IWMProfile2 interface [windows Media Format],AddMutualExclusion method, IWMProfile2::AddMutualExclusion, IWMProfile3 interface [windows Media Format],AddMutualExclusion method, IWMProfile3::AddMutualExclusion, IWMProfile::AddMutualExclusion, IWMProfileAddMutualExclusion, wmformat.iwmprofile_addmutualexclusion, wmsdkidl/IWMProfile2::AddMutualExclusion, wmsdkidl/IWMProfile3::AddMutualExclusion, wmsdkidl/IWMProfile::AddMutualExclusion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMProfile.AddMutualExclusion
 - IWMProfile2.AddMutualExclusion
 - IWMProfile3.AddMutualExclusion
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfile::AddMutualExclusion


## -description



The <b>AddMutualExclusion</b> method adds a mutual exclusion object to the profile. Mutual exclusion objects are used to specify a set of streams, only one of which can be output at a time.




## -parameters




### -param pME [in]

Pointer to the <a href="https://msdn.microsoft.com/040635fb-de00-4c8c-9c39-c28c409311c3">IWMMutualExclusion</a> interface of the mutual exclusion object to include in the profile. You must configure the mutual exclusion object by using the methods of the <b>IWMMutualExclusion</b> interface prior to using this method to add the mutual exclusion object to the profile.


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
The parameter <i>pME</i> is <b>NULL</b>, or the mutual exclusion type is not CLSID_WMMUTEX_Bitrate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STREAM</b></dt>
</dl>
</td>
<td width="60%">
A stream number in the mutual exclusion object being added is not part of the profile.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>



<a href="https://msdn.microsoft.com/949bb57f-8656-420e-b317-8ca7eb977a4e">IWMProfile::GetMutualExclusion</a>



<a href="https://msdn.microsoft.com/eb453285-a4e5-48dd-a4d0-72d2e09badc2">IWMProfile::RemoveMutualExclusion</a>



<a href="https://msdn.microsoft.com/3a3f6763-a241-4bbd-a6e8-62041b05622d">Mutual Exclusion</a>
 

 

