---
UID: NN:comcat.ICatRegister
title: ICatRegister (comcat.h)
description: Provides methods for registering and unregistering component category information in the registry. This includes both the human-readable names of categories and the categories implemented/required by a given component or class.helpviewer_keywords: ["ICatRegister","ICatRegister interface [COM]","ICatRegister interface [COM]","described","_com_icatregister","com.icatregister","comcat/ICatRegister"]
old-location: com\icatregister.htm
tech.root: com
ms.assetid: 3f4f9beb-51db-407f-91ea-6e32ff5796ce
ms.date: 12/05/2018
ms.keywords: ICatRegister, ICatRegister interface [COM], ICatRegister interface [COM],described, _com_icatregister, com.icatregister, comcat/ICatRegister
f1_keywords:
- comcat/ICatRegister
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICatRegister interface


## -description


Provides methods for registering and unregistering component category information in the registry. This includes both the human-readable names of categories and the categories implemented/required by a given component or class.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatRegister</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICatRegister</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatregister-registercategories">RegisterCategories</a>
</td>
<td align="left" width="63%">
Registers one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatregister-registerclassimplcategories">RegisterClassImplCategories</a>
</td>
<td align="left" width="63%">
Registers the class as implementing one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatregister-registerclassreqcategories">RegisterClassReqCategories</a>
</td>
<td align="left" width="63%">
Registers the class as requiring one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatregister-unregistercategories">UnRegisterCategories</a>
</td>
<td align="left" width="63%">
Removes the registration of one or more component categories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatregister-unregisterclassimplcategories">UnRegisterClassImplCategories</a>
</td>
<td align="left" width="63%">
Removes one or more implemented category identifiers from a class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nf-comcat-icatregister-unregisterclassreqcategories">UnRegisterClassReqCategories</a>
</td>
<td align="left" width="63%">
Removes one or more required category identifiers from a class.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comcat/ns-comcat-categoryinfo">CATEGORYINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nn-comcat-icatinformation">ICatInformation</a>
 

 

