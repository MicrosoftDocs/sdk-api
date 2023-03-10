---
UID: NF:wmsdkidl.IWMProfileManager.LoadSystemProfile
title: IWMProfileManager::LoadSystemProfile (wmsdkidl.h)
description: The LoadSystemProfile method loads a system profile identified by its index. If you do not know the index of the desired system profile, you must use IWMProfileManager::LoadProfileByID. To load a custom profile, use IWMProfileManager::LoadProfileByData.
helpviewer_keywords: ["IWMProfileManager interface [windows Media Format]","LoadSystemProfile method","IWMProfileManager.LoadSystemProfile","IWMProfileManager::LoadSystemProfile","IWMProfileManagerLoadSystemProfile","LoadSystemProfile","LoadSystemProfile method [windows Media Format]","LoadSystemProfile method [windows Media Format]","IWMProfileManager interface","wmformat.iwmprofilemanager_loadsystemprofile","wmsdkidl/IWMProfileManager::LoadSystemProfile"]
old-location: wmformat\iwmprofilemanager_loadsystemprofile.htm
tech.root: wmformat
ms.assetid: 5de4bd41-953b-4f50-b495-1d852831ae34
ms.date: 12/05/2018
ms.keywords: IWMProfileManager interface [windows Media Format],LoadSystemProfile method, IWMProfileManager.LoadSystemProfile, IWMProfileManager::LoadSystemProfile, IWMProfileManagerLoadSystemProfile, LoadSystemProfile, LoadSystemProfile method [windows Media Format], LoadSystemProfile method [windows Media Format],IWMProfileManager interface, wmformat.iwmprofilemanager_loadsystemprofile, wmsdkidl/IWMProfileManager::LoadSystemProfile
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
 - IWMProfileManager::LoadSystemProfile
 - wmsdkidl/IWMProfileManager::LoadSystemProfile
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
 - IWMProfileManager.LoadSystemProfile
---

# IWMProfileManager::LoadSystemProfile


## -description

The <b>LoadSystemProfile</b> method loads a system profile identified by its index. If you do not know the index of the desired system profile, you must use <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid">IWMProfileManager::LoadProfileByID</a>. To load a custom profile, use <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata">IWMProfileManager::LoadProfileByData</a>.

## -parameters

### -param dwProfileIndex [in]

<b>DWORD</b> containing the profile index.

### -param ppProfile [out]

Pointer to a pointer to an <a href="/windows/desktop/wmformat/iwmprofile">IWMProfile</a> interface.

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

Because there are no system profiles for the Windows Media 9 Series codecs, this method is primarily useful for obtaining version 8 system profiles that you will convert to custom profiles using the Windows Media 9 Series codecs. For more information, see <a href="/windows/desktop/wmformat/reusing-stream-configurations">Reusing Stream Configurations</a>.

This method can be used with <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount">GetSystemProfileCount</a> to iterate through the system profiles.

Applications must not rely on the index of a profile (used in this call and elsewhere in the SDK) being a constant. Upgrades to the Windows Media Format components can cause these indexes to change. If an application must maintain a fixed profile, it must call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile2-getprofileid">IWMProfile2::GetProfileID</a> and <b>IWMProfileManager::LoadProfileByID</b>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>