---
UID: NN:wmsdkidl.IWMProfileManagerLanguage
title: IWMProfileManagerLanguage (wmsdkidl.h)
author: windows-sdk-content
description: The IWMProfileManagerLanguage interface controls the language of the system profiles parsed by the profile manager.An IWMProfileManagerLanguage interface exists for every profile manager object.
old-location: wmformat\iwmprofilemanagerlanguage.htm
tech.root: wmformat
ms.assetid: 54875162-65fe-4959-b567-38c17ba2894d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMProfileManagerLanguage, IWMProfileManagerLanguage interface [windows Media Format], IWMProfileManagerLanguage interface [windows Media Format],described, IWMProfileManagerLanguageInterface, wmformat.iwmprofilemanagerlanguage, wmsdkidl/IWMProfileManagerLanguage
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
 - IWMProfileManagerLanguage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfileManagerLanguage interface


## -description



The <b>IWMProfileManagerLanguage</b> interface controls the language of the system profiles parsed by the profile manager.

An <b>IWMProfileManagerLanguage</b> interface exists for every profile manager object. You can obtain a pointer to an instance of this method by calling the <b>QueryInterface</b> method of any other interface of the profile manager object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProfileManagerLanguage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMProfileManagerLanguage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMProfileManagerLanguage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757390(v=VS.85).aspx">GetUserLanguageID</a>
</td>
<td align="left" width="63%">
Retrieves the language identifier of the system profiles currently loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757391(v=VS.85).aspx">SetUserLanguageID</a>
</td>
<td align="left" width="63%">
Specifies which set of system profiles to load based upon language.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd757385(v=VS.85).aspx">IWMProfileManager</a>
</td>
<td>IID_IWMProfileManager</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757386(v=VS.85).aspx">IWMProfileManager2</a>
</td>
<td>IID_IWMProfileManager2</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757385(v=VS.85).aspx">IWMProfileManager Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>
 

 

