---
UID: NN:comcat.ICatRegister
title: ICatRegister
author: windows-driver-content
description: Provides methods for registering and unregistering component category information in the registry. This includes both the human-readable names of categories and the categories implemented/required by a given component or class.
old-location: com\icatregister.htm
old-project: com
ms.assetid: 3f4f9beb-51db-407f-91ea-6e32ff5796ce
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ICatRegister, ICatRegister interface [COM], ICatRegister interface [COM], described, _com_icatregister, com.icatregister, comcat/ICatRegister
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ServerInformation, *PServerInformation
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComCat.h
api_name:
-	ICatRegister
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatRegister interface


## -description


Provides methods for registering and unregistering component category information in the registry. This includes both the human-readable names of categories and the categories implemented/required by a given component or class.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatRegister</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ICatRegister</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/c84a4b00-c43d-488a-b406-3bac2d25dcb8">RegisterCategories</a>
</td>
<td align="left" width="63%">
Registers one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c293038f-4dbf-40af-9237-c9bb59c84252">RegisterClassImplCategories</a>
</td>
<td align="left" width="63%">
Registers the class as implementing one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56aa5fcd-b46a-4807-ba51-9b4b6d28ceeb">RegisterClassReqCategories</a>
</td>
<td align="left" width="63%">
Registers the class as requiring one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29b7df20-bab0-419c-a13b-132ee5b0272d">UnRegisterCategories</a>
</td>
<td align="left" width="63%">
Removes the registration of one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a227fd1-6cbc-4354-a3e2-04aceb73ab65">UnRegisterClassImplCategories</a>
</td>
<td align="left" width="63%">
Removes one or more implemented category identifiers from a class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d957bc13-f5f7-4cb3-925e-4867ba9622cd">UnRegisterClassReqCategories</a>
</td>
<td align="left" width="63%">
Removes one or more required category identifiers from a class.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a5f0cb04-595d-4388-8943-79b9da76022b">CATEGORYINFO</a>



<a href="https://msdn.microsoft.com/1fd68126-b512-4131-8e93-cea7c1c3e9c0">ICatInformation</a>
 

 

