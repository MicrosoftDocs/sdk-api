---
UID: NF:wmsdkidl.IWMProfileManager.LoadSystemProfile
title: IWMProfileManager::LoadSystemProfile
author: windows-driver-content
description: The LoadSystemProfile method loads a system profile identified by its index. If you do not know the index of the desired system profile, you must use IWMProfileManager::LoadProfileByID. To load a custom profile, use IWMProfileManager::LoadProfileByData.
old-location: wmformat\iwmprofilemanager_loadsystemprofile.htm
old-project: wmformat
ms.assetid: 5de4bd41-953b-4f50-b495-1d852831ae34
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWMProfileManager interface [windows Media Format],LoadSystemProfile method, IWMProfileManager.LoadSystemProfile, IWMProfileManager::LoadSystemProfile, IWMProfileManagerLoadSystemProfile, LoadSystemProfile, LoadSystemProfile method [windows Media Format], LoadSystemProfile method [windows Media Format],IWMProfileManager interface, wmformat.iwmprofilemanager_loadsystemprofile, wmsdkidl/IWMProfileManager::LoadSystemProfile
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMProfileManager.LoadSystemProfile
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfileManager::LoadSystemProfile


## -description



The <b>LoadSystemProfile</b> method loads a system profile identified by its index. If you do not know the index of the desired system profile, you must use <a href="https://msdn.microsoft.com/16104e70-c800-49a6-a9cf-2b4669c865eb">IWMProfileManager::LoadProfileByID</a>. To load a custom profile, use <a href="https://msdn.microsoft.com/c645b6cc-e10d-4335-91c4-8bfd430ca76b">IWMProfileManager::LoadProfileByData</a>.




## -parameters




### -param dwProfileIndex [in]

<b>DWORD</b> containing the profile index.


### -param ppProfile [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile</a> interface.


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



Because there are no system profiles for the Windows Media 9 Series codecs, this method is primarily useful for obtaining version 8 system profiles that you will convert to custom profiles using the Windows Media 9 Series codecs. For more information, see <a href="https://msdn.microsoft.com/e2263c3a-56cd-4505-acd7-510dc7bac166">Reusing Stream Configurations</a>.

This method can be used with <a href="https://msdn.microsoft.com/895fa99d-66a5-4f5f-82ce-394264a945f7">GetSystemProfileCount</a> to iterate through the system profiles.

Applications must not rely on the index of a profile (used in this call and elsewhere in the SDK) being a constant. Upgrades to the Windows Media Format components can cause these indexes to change. If an application must maintain a fixed profile, it must call <a href="https://msdn.microsoft.com/82e3e086-4b19-4eb9-91ad-d30392f97a28">IWMProfile2::GetProfileID</a> and <b>IWMProfileManager::LoadProfileByID</b>.




## -see-also




<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager Interface</a>
 

 

