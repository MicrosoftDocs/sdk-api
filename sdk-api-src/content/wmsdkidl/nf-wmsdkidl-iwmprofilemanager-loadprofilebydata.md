---
UID: NF:wmsdkidl.IWMProfileManager.LoadProfileByData
title: IWMProfileManager::LoadProfileByData (wmsdkidl.h)
description: The LoadProfileByData method creates a profile object and populates it with data from a stored string. You must use this method to manipulate custom profiles. System profiles should be accessed using either LoadProfileByID or LoadSystemProfile.
helpviewer_keywords: ["IWMProfileManager interface [windows Media Format]","LoadProfileByData method","IWMProfileManager.LoadProfileByData","IWMProfileManager::LoadProfileByData","IWMProfileManagerLoadProfileByData","LoadProfileByData","LoadProfileByData method [windows Media Format]","LoadProfileByData method [windows Media Format]","IWMProfileManager interface","wmformat.iwmprofilemanager_loadprofilebydata","wmsdkidl/IWMProfileManager::LoadProfileByData"]
old-location: wmformat\iwmprofilemanager_loadprofilebydata.htm
tech.root: wmformat
ms.assetid: c645b6cc-e10d-4335-91c4-8bfd430ca76b
ms.date: 4/26/2023
ms.keywords: IWMProfileManager interface [windows Media Format],LoadProfileByData method, IWMProfileManager.LoadProfileByData, IWMProfileManager::LoadProfileByData, IWMProfileManagerLoadProfileByData, LoadProfileByData, LoadProfileByData method [windows Media Format], LoadProfileByData method [windows Media Format],IWMProfileManager interface, wmformat.iwmprofilemanager_loadprofilebydata, wmsdkidl/IWMProfileManager::LoadProfileByData
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
 - IWMProfileManager::LoadProfileByData
 - wmsdkidl/IWMProfileManager::LoadProfileByData
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
 - IWMProfileManager.LoadProfileByData
---

# IWMProfileManager::LoadProfileByData


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>LoadProfileByData</b> method creates a profile object and populates it with data from a stored string. You must use this method to manipulate custom profiles. System profiles should be accessed using either <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid">LoadProfileByID</a> or <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile">LoadSystemProfile</a>.

## -parameters

### -param pwszProfile [in]

Pointer to a wide-character <b>null</b>-terminated string containing the profile. Profile strings are limited to 153600 wide characters.

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
Either the <i>ppProfile</i> or <i>pwszProfile</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This string must match an XML-formatted string created by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile">IWMProfileManager::SaveProfile</a>. By convention, when such strings are saved to disk they are given the ".prx" extension.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>