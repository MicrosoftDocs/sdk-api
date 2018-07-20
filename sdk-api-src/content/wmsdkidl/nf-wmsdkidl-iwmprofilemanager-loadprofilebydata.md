---
UID: NF:wmsdkidl.IWMProfileManager.LoadProfileByData
title: IWMProfileManager::LoadProfileByData
author: windows-sdk-content
description: The LoadProfileByData method creates a profile object and populates it with data from a stored string. You must use this method to manipulate custom profiles. System profiles should be accessed using either LoadProfileByID or LoadSystemProfile.
old-location: wmformat\iwmprofilemanager_loadprofilebydata.htm
old-project: wmformat
ms.assetid: c645b6cc-e10d-4335-91c4-8bfd430ca76b
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMProfileManager interface [windows Media Format],LoadProfileByData method, IWMProfileManager.LoadProfileByData, IWMProfileManager::LoadProfileByData, IWMProfileManagerLoadProfileByData, LoadProfileByData, LoadProfileByData method [windows Media Format], LoadProfileByData method [windows Media Format],IWMProfileManager interface, wmformat.iwmprofilemanager_loadprofilebydata, wmsdkidl/IWMProfileManager::LoadProfileByData
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
api_name:
 - IWMProfileManager.LoadProfileByData
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfileManager::LoadProfileByData


## -description



The <b>LoadProfileByData</b> method creates a profile object and populates it with data from a stored string. You must use this method to manipulate custom profiles. System profiles should be accessed using either <a href="https://msdn.microsoft.com/16104e70-c800-49a6-a9cf-2b4669c865eb">LoadProfileByID</a> or <a href="https://msdn.microsoft.com/5de4bd41-953b-4f50-b495-1d852831ae34">LoadSystemProfile</a>.




## -parameters




### -param pwszProfile [in]

Pointer to a wide-character <b>null</b>-terminated string containing the profile. Profile strings are limited to 153600 wide characters.


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
Either the <i>ppProfile</i> or <i>pwszProfile</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This string must match an XML-formatted string created by <a href="https://msdn.microsoft.com/806def9b-1842-4443-9a63-fba380545018">IWMProfileManager::SaveProfile</a>. By convention, when such strings are saved to disk they are given the ".prx" extension.




## -see-also




<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager Interface</a>
 

 

