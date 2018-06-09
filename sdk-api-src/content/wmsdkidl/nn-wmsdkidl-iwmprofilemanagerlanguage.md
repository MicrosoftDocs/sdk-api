---
UID: NN:wmsdkidl.IWMProfileManagerLanguage
title: IWMProfileManagerLanguage
author: windows-sdk-content
description: The IWMProfileManagerLanguage interface controls the language of the system profiles parsed by the profile manager.An IWMProfileManagerLanguage interface exists for every profile manager object.
old-location: wmformat\iwmprofilemanagerlanguage.htm
old-project: wmformat
ms.assetid: 54875162-65fe-4959-b567-38c17ba2894d
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWMProfileManagerLanguage, IWMProfileManagerLanguage interface [windows Media Format], IWMProfileManagerLanguage interface [windows Media Format],described, IWMProfileManagerLanguageInterface, wmformat.iwmprofilemanagerlanguage, wmsdkidl/IWMProfileManagerLanguage
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
 - IWMProfileManagerLanguage
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/92d18ac9-8f68-47c6-91d7-de7653df69a6">GetUserLanguageID</a>
</td>
<td align="left" width="63%">
Retrieves the language identifier of the system profiles currently loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2154057-ea76-43bb-92d9-b52f16eb6b1b">SetUserLanguageID</a>
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
<a href="https://msdn.microsoft.com/eb5d904e-15ee-4066-ab05-c4e133bc89d7">IWMProfileManager2</a>
</td>
<td>IID_IWMProfileManager2</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>
 

 

