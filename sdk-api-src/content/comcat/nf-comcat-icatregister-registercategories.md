---
UID: NF:comcat.ICatRegister.RegisterCategories
title: ICatRegister::RegisterCategories (comcat.h)
author: windows-sdk-content
description: Registers one or more component categories. Each component category consists of a CATID and a list of locale-dependent description strings.
old-location: com\icatregister_registercategories.htm
tech.root: com
ms.assetid: c84a4b00-c43d-488a-b406-3bac2d25dcb8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICatRegister interface [COM],RegisterCategories method, ICatRegister.RegisterCategories, ICatRegister::RegisterCategories, RegisterCategories, RegisterCategories method [COM], RegisterCategories method [COM],ICatRegister interface, _com_icatregister_registercategories, com.icatregister_registercategories, comcat/ICatRegister::RegisterCategories
ms.topic: method
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
 - ICatRegister.RegisterCategories
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICatRegister::RegisterCategories


## -description


Registers one or more component categories. Each component category consists of a CATID and a list of locale-dependent description strings.


## -parameters




### -param cCategories [in]

The number of component categories to be registered.


### -param rgCategoryInfo [in]

An array of <a href="https://msdn.microsoft.com/a5f0cb04-595d-4388-8943-79b9da76022b">CATEGORYINFO</a> structures, one for each category to be registered. By providing the same CATID for multiple <b>CATEGORYINFO</b> structures, multiple locales can be registered for the same component category.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are incorrect.

</td>
</tr>
</table>
 




## -remarks



This method can only be called by the owner of a category, usually as part of the installation or de-installation of the operating system or application.




## -see-also




<a href="https://msdn.microsoft.com/3f4f9beb-51db-407f-91ea-6e32ff5796ce">ICatRegister</a>
 

 

