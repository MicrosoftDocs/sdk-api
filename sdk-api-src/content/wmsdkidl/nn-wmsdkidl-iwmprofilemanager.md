---
UID: NN:wmsdkidl.IWMProfileManager
title: IWMProfileManager (wmsdkidl.h)
author: windows-sdk-content
description: The IWMProfileManager interface is used to create profiles, load existing profiles, and save profiles.
old-location: wmformat\iwmprofilemanager.htm
tech.root: wmformat
ms.assetid: e5ec945c-4513-48ad-8bef-e0fb54826991
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMProfileManager, IWMProfileManager interface [windows Media Format], IWMProfileManager interface [windows Media Format],described, IWMProfileManagerInterface, wmformat.iwmprofilemanager, wmsdkidl/IWMProfileManager
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMProfileManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfileManager interface


## -description



The <b>IWMProfileManager</b> interface is used to create profiles, load existing profiles, and save profiles. It can be used with both system profiles and application-defined custom profiles. To make changes to a profile, you must load it into a profile object using one of the loading methods of this interface. You can then access the profile data through the use of the interfaces of the profile object.

<b>IWMProfileManager</b> is the default interface of a profile manager object. When you create a new profile manager object using the <a href="https://msdn.microsoft.com/en-us/library/Dd757762(v=VS.85).aspx">WMCreateProfileManager</a> function, you obtain a pointer to <b>IWMProfileManager</b>.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd757392(v=VS.85).aspx">CreateEmptyProfile</a>
</td>
<td align="left" width="63%">
Creates an empty profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757393(v=VS.85).aspx">GetSystemProfileCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of system profiles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757394(v=VS.85).aspx">LoadProfileByData</a>
</td>
<td align="left" width="63%">
Creates a profile object and populates it with the data from an existing profile that has been saved to a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757395(v=VS.85).aspx">LoadProfileByID</a>
</td>
<td align="left" width="63%">
Creates a profile object and populates it with the data from a system profile. Uses the GUID to find the profile data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757396(v=VS.85).aspx">LoadSystemProfile</a>
</td>
<td align="left" width="63%">
Creates a profile object and populates it with data from a system profile. Uses the profile's index to find the profile data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757397(v=VS.85).aspx">SaveProfile</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd743313(v=VS.85).aspx">IWMCodecInfo</a>
</td>
<td>IID_IWMCodecInfo</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd743314(v=VS.85).aspx">IWMCodecInfo2</a>
</td>
<td>IID_IWMCodecInfo2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd743317(v=VS.85).aspx">IWMCodecInfo3</a>
</td>
<td>IID_IWMCodecInfo3</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757386(v=VS.85).aspx">IWMProfileManager2</a>
</td>
<td>IID_IWMProfileManager2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757389(v=VS.85).aspx">IWMProfileManagerLanguage</a>
</td>
<td>IID_IWMProfileManagerLanguage</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757386(v=VS.85).aspx">IWMProfileManager2 Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>



<a href="https://msdn.microsoft.com/ec42889e-580e-4a65-9fe6-4a5f15c97eb0">Profile Object</a>



<a href="https://msdn.microsoft.com/4e0f3a40-68d6-452e-8e6a-c9e79504ccb6">Using System Profiles</a>



<a href="https://msdn.microsoft.com/e1e31632-0db7-47db-a992-f5db9d8824c1">Working with Profiles</a>
 

 

