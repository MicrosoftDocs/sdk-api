---
UID: NF:wmsdkidl.IWMProfileManager.GetSystemProfileCount
title: IWMProfileManager::GetSystemProfileCount
author: windows-driver-content
description: The GetSystemProfileCount method retrieves the number of system profiles.
old-location: wmformat\iwmprofilemanager_getsystemprofilecount.htm
old-project: wmformat
ms.assetid: 895fa99d-66a5-4f5f-82ce-394264a945f7
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetSystemProfileCount, GetSystemProfileCount method [windows Media Format], GetSystemProfileCount method [windows Media Format],IWMProfileManager interface, IWMProfileManager interface [windows Media Format],GetSystemProfileCount method, IWMProfileManager.GetSystemProfileCount, IWMProfileManager::GetSystemProfileCount, IWMProfileManagerGetSystemProfileCount, wmformat.iwmprofilemanager_getsystemprofilecount, wmsdkidl/IWMProfileManager::GetSystemProfileCount
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
-	IWMProfileManager.GetSystemProfileCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



Because there are no system profiles for the Windows Media 9 Series codecs, this method is primarily useful for obtaining version 8 system profiles that you will convert to custom profiles using the Windows Media 9 Series codecs. For more information, see <a href="https://msdn.microsoft.com/e2263c3a-56cd-4505-acd7-510dc7bac166">Reusing Stream Configurations</a>.

This method can be used with <a href="https://msdn.microsoft.com/5de4bd41-953b-4f50-b495-1d852831ae34">LoadSystemProfile</a> to iterate through the system profiles.

The <a href="https://msdn.microsoft.com/cd957f3b-401c-4ab1-9c54-7b4ac895caac">IWMProfileManager2::SetSystemProfileVersion</a> method determines which system files are enumerated. Most applications should set the version to WMT_VER_8_0. Setting the version to WMT_VER_9_0 will return zero profiles.




## -see-also




<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager Interface</a>
 

 

