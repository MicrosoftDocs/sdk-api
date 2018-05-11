---
UID: NN:wmsdkidl.IWMProfileManager
title: IWMProfileManager
author: windows-driver-content
description: The IWMProfileManager interface is used to create profiles, load existing profiles, and save profiles.
old-location: wmformat\iwmprofilemanager.htm
old-project: wmformat
ms.assetid: e5ec945c-4513-48ad-8bef-e0fb54826991
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWMProfileManager, IWMProfileManager interface [windows Media Format], IWMProfileManager interface [windows Media Format],described, IWMProfileManagerInterface, wmformat.iwmprofilemanager, wmsdkidl/IWMProfileManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	wmsdkidl.h
api_name:
-	IWMProfileManager
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfileManager interface


## -description



The <b>IWMProfileManager</b> interface is used to create profiles, load existing profiles, and save profiles. It can be used with both system profiles and application-defined custom profiles. To make changes to a profile, you must load it into a profile object using one of the loading methods of this interface. You can then access the profile data through the use of the interfaces of the profile object.

<b>IWMProfileManager</b> is the default interface of a profile manager object. When you create a new profile manager object using the <a href="https://msdn.microsoft.com/77eea431-74a0-449e-847e-7885ab33bda1">WMCreateProfileManager</a> function, you obtain a pointer to <b>IWMProfileManager</b>.

<div class="alert"><b>Note</b>  When a profile manager object is created it parses all of the system profiles. Creating and releasing a profile manager every time you need to use it will adversely affect performance. You should create a profile manager once in your application and release it only when you no longer need to use it.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProfileManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMProfileManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMProfileManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb5c2ed4-f733-422e-87e3-8e70c3ee9f1c">CreateEmptyProfile</a>
</td>
<td align="left" width="63%">
Creates an empty profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/895fa99d-66a5-4f5f-82ce-394264a945f7">GetSystemProfileCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of system profiles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c645b6cc-e10d-4335-91c4-8bfd430ca76b">LoadProfileByData</a>
</td>
<td align="left" width="63%">
Creates a profile object and populates it with the data from an existing profile that has been saved to a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16104e70-c800-49a6-a9cf-2b4669c865eb">LoadProfileByID</a>
</td>
<td align="left" width="63%">
Creates a profile object and populates it with the data from a system profile. Uses the GUID to find the profile data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5de4bd41-953b-4f50-b495-1d852831ae34">LoadSystemProfile</a>
</td>
<td align="left" width="63%">
Creates a profile object and populates it with data from a system profile. Uses the profile's index to find the profile data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/806def9b-1842-4443-9a63-fba380545018">SaveProfile</a>
</td>
<td align="left" width="63%">
Saves a custom profile into a string. You can save the profile to disk by copying the string into a .prx file.

</td>
</tr>
</table> 


    The following interfaces can be obtained by using the QueryInterface method of this interface.<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/70661d13-737a-4e83-94e6-9a1af07b0369">IWMCodecInfo</a>
</td>
<td>IID_IWMCodecInfo</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/0cfb355e-af68-400d-aa64-57f17e7d936b">IWMCodecInfo2</a>
</td>
<td>IID_IWMCodecInfo2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/fd882612-1f60-4b51-a180-0d34d78c99dd">IWMCodecInfo3</a>
</td>
<td>IID_IWMCodecInfo3</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/eb5d904e-15ee-4066-ab05-c4e133bc89d7">IWMProfileManager2</a>
</td>
<td>IID_IWMProfileManager2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/54875162-65fe-4959-b567-38c17ba2894d">IWMProfileManagerLanguage</a>
</td>
<td>IID_IWMProfileManagerLanguage</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/eb5d904e-15ee-4066-ab05-c4e133bc89d7">IWMProfileManager2 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>



<a href="https://msdn.microsoft.com/ec42889e-580e-4a65-9fe6-4a5f15c97eb0">Profile Object</a>



<a href="https://msdn.microsoft.com/4e0f3a40-68d6-452e-8e6a-c9e79504ccb6">Using System Profiles</a>



<a href="https://msdn.microsoft.com/e1e31632-0db7-47db-a992-f5db9d8824c1">Working with Profiles</a>
 

 

