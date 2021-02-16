---
UID: NF:comcat.ICatRegister.UnRegisterCategories
title: ICatRegister::UnRegisterCategories (comcat.h)
description: Removes the registration of one or more component categories. Each component category consists of a CATID and a list of locale-dependent description strings.
helpviewer_keywords: ["ICatRegister interface [COM]","UnRegisterCategories method","ICatRegister.UnRegisterCategories","ICatRegister::UnRegisterCategories","UnRegisterCategories","UnRegisterCategories method [COM]","UnRegisterCategories method [COM]","ICatRegister interface","_com_icatregister_unregistercategories","com.icatregister_unregistercategories","comcat/ICatRegister::UnRegisterCategories"]
old-location: com\icatregister_unregistercategories.htm
tech.root: com
ms.assetid: 29b7df20-bab0-419c-a13b-132ee5b0272d
ms.date: 12/05/2018
ms.keywords: ICatRegister interface [COM],UnRegisterCategories method, ICatRegister.UnRegisterCategories, ICatRegister::UnRegisterCategories, UnRegisterCategories, UnRegisterCategories method [COM], UnRegisterCategories method [COM],ICatRegister interface, _com_icatregister_unregistercategories, com.icatregister_unregistercategories, comcat/ICatRegister::UnRegisterCategories
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICatRegister::UnRegisterCategories
 - comcat/ICatRegister::UnRegisterCategories
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComCat.h
api_name:
 - ICatRegister.UnRegisterCategories
---

# ICatRegister::UnRegisterCategories


## -description

Removes the registration of one or more component categories. Each component category consists of a CATID and a list of locale-dependent description strings.

## -parameters

### -param cCategories [in]

The number of categories to be removed.

### -param rgcatid [in]

The CATIDs of the categories to be removed.

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

This method will be successful even if one or more of the category IDs specified are not registered. This method can only be called by the owner of a category, usually as part of the installation or de-installation of the operating system or application.

This method does not remove the component category tags from individual classes. To do this, use the <a href="/windows/desktop/api/comcat/nf-comcat-icatregister-unregisterclassreqcategories">ICatRegister::UnRegisterClassReqCategories</a> method.

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-icatregister">ICatRegister</a>