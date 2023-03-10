---
UID: NF:comcat.ICatRegister.RegisterClassImplCategories
title: ICatRegister::RegisterClassImplCategories (comcat.h)
description: Registers the class as implementing one or more component categories.
helpviewer_keywords: ["ICatRegister interface [COM]","RegisterClassImplCategories method","ICatRegister.RegisterClassImplCategories","ICatRegister::RegisterClassImplCategories","RegisterClassImplCategories","RegisterClassImplCategories method [COM]","RegisterClassImplCategories method [COM]","ICatRegister interface","_com_icatregister_registerclassimplcategories","com.icatregister_registerclassimplcategories","comcat/ICatRegister::RegisterClassImplCategories"]
old-location: com\icatregister_registerclassimplcategories.htm
tech.root: com
ms.assetid: c293038f-4dbf-40af-9237-c9bb59c84252
ms.date: 12/05/2018
ms.keywords: ICatRegister interface [COM],RegisterClassImplCategories method, ICatRegister.RegisterClassImplCategories, ICatRegister::RegisterClassImplCategories, RegisterClassImplCategories, RegisterClassImplCategories method [COM], RegisterClassImplCategories method [COM],ICatRegister interface, _com_icatregister_registerclassimplcategories, com.icatregister_registerclassimplcategories, comcat/ICatRegister::RegisterClassImplCategories
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
 - ICatRegister::RegisterClassImplCategories
 - comcat/ICatRegister::RegisterClassImplCategories
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
 - ICatRegister.RegisterClassImplCategories
---

# ICatRegister::RegisterClassImplCategories


## -description

Registers the class as implementing one or more component categories.

## -parameters

### -param rclsid [in]

The class identifier.

### -param cCategories [in]

The number of categories to be associated as category identifiers for the class.

### -param rgcatid [in]

An array of CATIDs to associate as category identifiers for the class.

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

In case of an error, this method does not ensure that the registry is restored to the state prior to the call. This method can only be called by the owner of a class, usually as part of the installation of the component.

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-icatregister">ICatRegister</a>