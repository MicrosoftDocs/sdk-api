---
UID: NN:wmsdkidl.IWMProfileManager2
title: IWMProfileManager2
author: windows-sdk-content
description: The IWMProfileManager2 interface adds methods to specify and retrieve the version number of the system profiles enumerated by the profile manager.
old-location: wmformat\iwmprofilemanager2.htm
old-project: wmformat
ms.assetid: eb5d904e-15ee-4066-ab05-c4e133bc89d7
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMProfileManager2, IWMProfileManager2 interface [windows Media Format], IWMProfileManager2 interface [windows Media Format],described, IWMProfileManager2Interface, wmformat.iwmprofilemanager2, wmsdkidl/IWMProfileManager2
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMProfileManager2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfileManager2 interface


## -description



The <b>IWMProfileManager2</b> interface adds methods to specify and retrieve the version number of the system profiles enumerated by the profile manager. Most applications should set the value to the latest version unless they need to be backward-compatible with another application that was written using an earlier version of this SDK.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProfileManager2</b> interface inherits from <a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager</a>. <b>IWMProfileManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMProfileManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/155b847b-81c0-4065-ae00-ca0b64cdd537">GetSystemProfileVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version number of the system profiles that the profile manager enumerates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd957f3b-401c-4ab1-9c54-7b4ac895caac">SetSystemProfileVersion</a>
</td>
<td align="left" width="63%">
Specifies the version number of the system profiles that the profile manager enumerates.

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
<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager</a>
</td>
<td>IID_IWMProfileManager</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/54875162-65fe-4959-b567-38c17ba2894d">IWMProfileManagerLanguage</a>
</td>
<td>IID_IWMProfileManagerLanguage</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>



<a href="https://msdn.microsoft.com/e1e31632-0db7-47db-a992-f5db9d8824c1">Working with Profiles</a>
 

 

