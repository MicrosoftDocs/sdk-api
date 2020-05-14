---
UID: NF:wmsdkidl.IWMProfileManager.CreateEmptyProfile
title: IWMProfileManager::CreateEmptyProfile (wmsdkidl.h)
description: The CreateEmptyProfile method creates an empty profile object. You can use the interfaces of the profile object to configure the profile. When you are done configuring the profile, you can save it to a string using IWMProfileManager::SaveProfile.helpviewer_keywords: ["CreateEmptyProfile","CreateEmptyProfile method [windows Media Format]","CreateEmptyProfile method [windows Media Format]","IWMProfileManager interface","IWMProfileManager interface [windows Media Format]","CreateEmptyProfile method","IWMProfileManager.CreateEmptyProfile","IWMProfileManager::CreateEmptyProfile","IWMProfileManagerCreateEmptyProfile","wmformat.iwmprofilemanager_createemptyprofile","wmsdkidl/IWMProfileManager::CreateEmptyProfile"]
old-location: wmformat\iwmprofilemanager_createemptyprofile.htm
tech.root: wmformat
ms.assetid: fb5c2ed4-f733-422e-87e3-8e70c3ee9f1c
ms.date: 12/05/2018
ms.keywords: CreateEmptyProfile, CreateEmptyProfile method [windows Media Format], CreateEmptyProfile method [windows Media Format],IWMProfileManager interface, IWMProfileManager interface [windows Media Format],CreateEmptyProfile method, IWMProfileManager.CreateEmptyProfile, IWMProfileManager::CreateEmptyProfile, IWMProfileManagerCreateEmptyProfile, wmformat.iwmprofilemanager_createemptyprofile, wmsdkidl/IWMProfileManager::CreateEmptyProfile
f1_keywords:
- wmsdkidl/IWMProfileManager.CreateEmptyProfile
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
api_name:
- IWMProfileManager.CreateEmptyProfile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfileManager::CreateEmptyProfile


## -description



The <b>CreateEmptyProfile</b> method creates an empty profile object. You can use the interfaces of the profile object to configure the profile. When you are done configuring the profile, you can save it to a string using <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile">IWMProfileManager::SaveProfile</a>.




## -parameters




### -param dwVersion [in]

<b>DWORD</b> containing one member of the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_version">WMT_VERSION</a> enumeration type.


### -param ppProfile [out]

Pointer to a pointer to an <a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile</a> interface.


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
There is not enough available memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppProfile</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Use this method to create any profile that uses the Windows Media® Audio and Video 9 Series codecs. For more information, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/reusing-stream-configurations">Reusing Stream Configurations</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_version">WMT_VERSION</a>
 

 

