---
UID: NF:wmsdkidl.IWMProfileManager.CreateEmptyProfile
title: IWMProfileManager::CreateEmptyProfile method
author: windows-driver-content
description: The CreateEmptyProfile method creates an empty profile object. You can use the interfaces of the profile object to configure the profile. When you are done configuring the profile, you can save it to a string using IWMProfileManager::SaveProfile.
old-location: wmformat\iwmprofilemanager_createemptyprofile.htm
old-project: wmformat
ms.assetid: fb5c2ed4-f733-422e-87e3-8e70c3ee9f1c
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: CreateEmptyProfile method [windows Media Format], CreateEmptyProfile method [windows Media Format], IWMProfileManager interface, CreateEmptyProfile,IWMProfileManager.CreateEmptyProfile, IWMProfileManager, IWMProfileManager interface [windows Media Format], CreateEmptyProfile method, IWMProfileManager::CreateEmptyProfile, IWMProfileManagerCreateEmptyProfile, wmformat.iwmprofilemanager_createemptyprofile, wmsdkidl/IWMProfileManager::CreateEmptyProfile
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
-	IWMProfileManager.CreateEmptyProfile
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfileManager::CreateEmptyProfile method


## -description



The <b>CreateEmptyProfile</b> method creates an empty profile object. You can use the interfaces of the profile object to configure the profile. When you are done configuring the profile, you can save it to a string using <a href="https://msdn.microsoft.com/806def9b-1842-4443-9a63-fba380545018">IWMProfileManager::SaveProfile</a>.




## -parameters




### -param dwVersion [in]

<b>DWORD</b> containing one member of the <a href="https://msdn.microsoft.com/9ee414c6-49aa-42ad-9310-52f54b23e712">WMT_VERSION</a> enumeration type.


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



Use this method to create any profile that uses the Windows Media® Audio and Video 9 Series codecs. For more information, see <a href="https://msdn.microsoft.com/e2263c3a-56cd-4505-acd7-510dc7bac166">Reusing Stream Configurations</a>.




## -see-also




<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager Interface</a>



<a href="https://msdn.microsoft.com/9ee414c6-49aa-42ad-9310-52f54b23e712">WMT_VERSION</a>
 

 

