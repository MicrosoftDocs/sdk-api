---
UID: NN:comcat.ICatRegister
title: ICatRegister
author: windows-sdk-content
description: Provides methods for registering and unregistering component category information in the registry. This includes both the human-readable names of categories and the categories implemented/required by a given component or class.
old-location: com\icatregister.htm
tech.root: com
ms.assetid: 3f4f9beb-51db-407f-91ea-6e32ff5796ce
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: ICatRegister, ICatRegister interface [COM], ICatRegister interface [COM],described, _com_icatregister, com.icatregister, comcat/ICatRegister
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComCat.idl
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
 - ComCat.h
api_name:
 - ICatRegister
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICatRegister interface


## -description


Provides methods for registering and unregistering component category information in the registry. This includes both the human-readable names of categories and the categories implemented/required by a given component or class.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatRegister</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICatRegister</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICatRegister</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms692843(v=VS.85).aspx">RegisterCategories</a>
</td>
<td align="left" width="63%">
Registers one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms692674(v=VS.85).aspx">RegisterClassImplCategories</a>
</td>
<td align="left" width="63%">
Registers the class as implementing one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683712(v=VS.85).aspx">RegisterClassReqCategories</a>
</td>
<td align="left" width="63%">
Registers the class as requiring one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms680084(v=VS.85).aspx">UnRegisterCategories</a>
</td>
<td align="left" width="63%">
Removes the registration of one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682292(v=VS.85).aspx">UnRegisterClassImplCategories</a>
</td>
<td align="left" width="63%">
Removes one or more implemented category identifiers from a class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms693463(v=VS.85).aspx">UnRegisterClassReqCategories</a>
</td>
<td align="left" width="63%">
Removes one or more required category identifiers from a class.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690475(v=VS.85).aspx">CATEGORYINFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd542655(v=VS.85).aspx">ICatInformation</a>
 

 

