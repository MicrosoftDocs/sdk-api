---
UID: NF:wmsdkidl.IWMProfile.AddMutualExclusion
title: IWMProfile::AddMutualExclusion (wmsdkidl.h)
description: The AddMutualExclusion method adds a mutual exclusion object to the profile. Mutual exclusion objects are used to specify a set of streams, only one of which can be output at a time.
helpviewer_keywords: ["AddMutualExclusion","AddMutualExclusion method [windows Media Format]","AddMutualExclusion method [windows Media Format]","IWMProfile interface","AddMutualExclusion method [windows Media Format]","IWMProfile2 interface","AddMutualExclusion method [windows Media Format]","IWMProfile3 interface","IWMProfile interface [windows Media Format]","AddMutualExclusion method","IWMProfile.AddMutualExclusion","IWMProfile2 interface [windows Media Format]","AddMutualExclusion method","IWMProfile2::AddMutualExclusion","IWMProfile3 interface [windows Media Format]","AddMutualExclusion method","IWMProfile3::AddMutualExclusion","IWMProfile::AddMutualExclusion","IWMProfileAddMutualExclusion","wmformat.iwmprofile_addmutualexclusion","wmsdkidl/IWMProfile2::AddMutualExclusion","wmsdkidl/IWMProfile3::AddMutualExclusion","wmsdkidl/IWMProfile::AddMutualExclusion"]
old-location: wmformat\iwmprofile_addmutualexclusion.htm
tech.root: wmformat
ms.assetid: efd751cf-d34d-4e74-9a00-444ec31ebef0
ms.date: 4/26/2023
ms.keywords: AddMutualExclusion, AddMutualExclusion method [windows Media Format], AddMutualExclusion method [windows Media Format],IWMProfile interface, AddMutualExclusion method [windows Media Format],IWMProfile2 interface, AddMutualExclusion method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],AddMutualExclusion method, IWMProfile.AddMutualExclusion, IWMProfile2 interface [windows Media Format],AddMutualExclusion method, IWMProfile2::AddMutualExclusion, IWMProfile3 interface [windows Media Format],AddMutualExclusion method, IWMProfile3::AddMutualExclusion, IWMProfile::AddMutualExclusion, IWMProfileAddMutualExclusion, wmformat.iwmprofile_addmutualexclusion, wmsdkidl/IWMProfile2::AddMutualExclusion, wmsdkidl/IWMProfile3::AddMutualExclusion, wmsdkidl/IWMProfile::AddMutualExclusion
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMProfile::AddMutualExclusion
 - wmsdkidl/IWMProfile::AddMutualExclusion
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
 - qasf.dll
api_name:
 - IWMProfile.AddMutualExclusion
 - IWMProfile2.AddMutualExclusion
 - IWMProfile3.AddMutualExclusion
---

# IWMProfile::AddMutualExclusion


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddMutualExclusion</b> method adds a mutual exclusion object to the profile. Mutual exclusion objects are used to specify a set of streams, only one of which can be output at a time.

## -parameters

### -param pME [in]

Pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion">IWMMutualExclusion</a> interface of the mutual exclusion object to include in the profile. You must configure the mutual exclusion object by using the methods of the <b>IWMMutualExclusion</b> interface prior to using this method to add the mutual exclusion object to the profile.

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

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion">IWMProfile::GetMutualExclusion</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion">IWMProfile::RemoveMutualExclusion</a>



<a href="/windows/desktop/wmformat/mutual-exclusion">Mutual Exclusion</a>