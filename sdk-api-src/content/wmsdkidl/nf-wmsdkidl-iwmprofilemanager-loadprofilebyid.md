---
UID: NF:wmsdkidl.IWMProfileManager.LoadProfileByID
title: IWMProfileManager::LoadProfileByID (wmsdkidl.h)
description: The LoadProfileByID method loads a system profile identified by its globally unique identifier. To load a custom profile, use IWMProfileManager::LoadProfileByData.
helpviewer_keywords: ["IWMProfileManager interface [windows Media Format]","LoadProfileByID method","IWMProfileManager.LoadProfileByID","IWMProfileManager::LoadProfileByID","IWMProfileManagerLoadProfileByID","LoadProfileByID","LoadProfileByID method [windows Media Format]","LoadProfileByID method [windows Media Format]","IWMProfileManager interface","wmformat.iwmprofilemanager_loadprofilebyid","wmsdkidl/IWMProfileManager::LoadProfileByID"]
old-location: wmformat\iwmprofilemanager_loadprofilebyid.htm
tech.root: wmformat
ms.assetid: 16104e70-c800-49a6-a9cf-2b4669c865eb
ms.date: 12/05/2018
ms.keywords: IWMProfileManager interface [windows Media Format],LoadProfileByID method, IWMProfileManager.LoadProfileByID, IWMProfileManager::LoadProfileByID, IWMProfileManagerLoadProfileByID, LoadProfileByID, LoadProfileByID method [windows Media Format], LoadProfileByID method [windows Media Format],IWMProfileManager interface, wmformat.iwmprofilemanager_loadprofilebyid, wmsdkidl/IWMProfileManager::LoadProfileByID
f1_keywords:
- wmsdkidl/IWMProfileManager.LoadProfileByID
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
- IWMProfileManager.LoadProfileByID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfileManager::LoadProfileByID


## -description



The <b>LoadProfileByID</b> method loads a system profile identified by its globally unique identifier. To load a custom profile, use <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata">IWMProfileManager::LoadProfileByData</a>.




## -parameters




### -param guidProfile [in]

<b>GUID</b> identifying the profile. For more information, see the table of defined constants in <a href="https://docs.microsoft.com/windows/desktop/wmformat/using-system-profiles">Using System Profiles</a>.


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



Only system profiles have IDs. Because there are no system profiles for the Windows Media 9 Series codecs, this method is primarily useful for obtaining version 8 system profiles that you will convert to custom profiles using the Windows Media 9 Series codecs. For more information, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/reusing-stream-configurations">Reusing Stream Configurations</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/using-system-profiles">Using System Profiles</a>
 

 

