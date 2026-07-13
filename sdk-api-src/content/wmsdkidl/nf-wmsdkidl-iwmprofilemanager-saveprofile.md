---
UID: NF:wmsdkidl.IWMProfileManager.SaveProfile
title: IWMProfileManager::SaveProfile (wmsdkidl.h)
description: The SaveProfile method saves a profile into an XML-formatted string.
helpviewer_keywords: ["IWMProfileManager interface [windows Media Format]","SaveProfile method","IWMProfileManager.SaveProfile","IWMProfileManager::SaveProfile","IWMProfileManagerSaveProfile","SaveProfile","SaveProfile method [windows Media Format]","SaveProfile method [windows Media Format]","IWMProfileManager interface","wmformat.iwmprofilemanager_saveprofile","wmsdkidl/IWMProfileManager::SaveProfile"]
old-location: wmformat\iwmprofilemanager_saveprofile.htm
tech.root: wmformat
ms.assetid: 806def9b-1842-4443-9a63-fba380545018
ms.date: 4/26/2023
ms.keywords: IWMProfileManager interface [windows Media Format],SaveProfile method, IWMProfileManager.SaveProfile, IWMProfileManager::SaveProfile, IWMProfileManagerSaveProfile, SaveProfile, SaveProfile method [windows Media Format], SaveProfile method [windows Media Format],IWMProfileManager interface, wmformat.iwmprofilemanager_saveprofile, wmsdkidl/IWMProfileManager::SaveProfile
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
 - IWMProfileManager::SaveProfile
 - wmsdkidl/IWMProfileManager::SaveProfile
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
 - IWMProfileManager.SaveProfile
---

# IWMProfileManager::SaveProfile


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SaveProfile</b> method saves a profile into an XML-formatted string.

## -parameters

### -param pIWMProfile [in]

Pointer to the <a href="/windows/desktop/wmformat/iwmprofile">IWMProfile</a> interface of the object containing the profile data to be saved.

### -param pwszProfile [in]

Pointer to a wide-character <b>null</b>-terminated string containing the profile. Set this to <b>NULL</b> to retrieve the length of string required.

### -param pdwLength [in, out]

On input, specifies the length of the <i>pwszProfile</i> string. On output, if the method succeeds, specifies a pointer to a <b>DWORD</b> containing the number of characters, including the terminating <b>null</b> character, required to hold the profile.

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
Either the <i>pIWMProfile</i> or <i>pdwLength</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>SaveProfile</b>. On the first call, pass <b>NULL</b> as <i>pwszProfile</i>. On return, the value of <i>pdwLength</i> is set to the length required to hold the profile in string form. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pwszProfile</i> on the second call.

This string contains all the profile information. It must not be displayed to users, and should not be altered. To change the settings in a saved profile, load it using the profile manager and change the settings using the profile object and related objects.

To save a custom profile for later use, you must save the content of the returned string in a .prx file. For more information on .prx files, see <a href="/windows/desktop/wmformat/profiles">Profiles</a>.

To load a saved custom profile, copy the contents of the profile from the .prx file to a string and use <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata">IWMProfileManager::LoadProfileByData</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>