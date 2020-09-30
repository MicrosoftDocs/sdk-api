---
UID: NF:wmsdkidl.IWMProfileManager.GetSystemProfileCount
title: IWMProfileManager::GetSystemProfileCount (wmsdkidl.h)
description: The GetSystemProfileCount method retrieves the number of system profiles.
helpviewer_keywords: ["GetSystemProfileCount","GetSystemProfileCount method [windows Media Format]","GetSystemProfileCount method [windows Media Format]","IWMProfileManager interface","IWMProfileManager interface [windows Media Format]","GetSystemProfileCount method","IWMProfileManager.GetSystemProfileCount","IWMProfileManager::GetSystemProfileCount","IWMProfileManagerGetSystemProfileCount","wmformat.iwmprofilemanager_getsystemprofilecount","wmsdkidl/IWMProfileManager::GetSystemProfileCount"]
old-location: wmformat\iwmprofilemanager_getsystemprofilecount.htm
tech.root: wmformat
ms.assetid: 895fa99d-66a5-4f5f-82ce-394264a945f7
ms.date: 12/05/2018
ms.keywords: GetSystemProfileCount, GetSystemProfileCount method [windows Media Format], GetSystemProfileCount method [windows Media Format],IWMProfileManager interface, IWMProfileManager interface [windows Media Format],GetSystemProfileCount method, IWMProfileManager.GetSystemProfileCount, IWMProfileManager::GetSystemProfileCount, IWMProfileManagerGetSystemProfileCount, wmformat.iwmprofilemanager_getsystemprofilecount, wmsdkidl/IWMProfileManager::GetSystemProfileCount
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
 - IWMProfileManager::GetSystemProfileCount
 - wmsdkidl/IWMProfileManager::GetSystemProfileCount
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
 - IWMProfileManager.GetSystemProfileCount
---

# IWMProfileManager::GetSystemProfileCount


## -description

The <b>GetSystemProfileCount</b> method retrieves the number of system profiles.

## -parameters

### -param pcProfiles [out]

Pointer to a count of the system profiles.

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
The <i>pcProfiles</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALIDPROFILE</b></dt>
</dl>
</td>
<td width="60%">
The system profiles could not be found.

</td>
</tr>
</table>

## -remarks

Because there are no system profiles for the Windows Media 9 Series codecs, this method is primarily useful for obtaining version 8 system profiles that you will convert to custom profiles using the Windows Media 9 Series codecs. For more information, see <a href="/windows/desktop/wmformat/reusing-stream-configurations">Reusing Stream Configurations</a>.

This method can be used with <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile">LoadSystemProfile</a> to iterate through the system profiles.

The <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager2-setsystemprofileversion">IWMProfileManager2::SetSystemProfileVersion</a> method determines which system files are enumerated. Most applications should set the version to WMT_VER_8_0. Setting the version to WMT_VER_9_0 will return zero profiles.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>