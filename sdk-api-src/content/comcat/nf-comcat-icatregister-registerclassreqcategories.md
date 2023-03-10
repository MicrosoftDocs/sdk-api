---
UID: NF:comcat.ICatRegister.RegisterClassReqCategories
title: ICatRegister::RegisterClassReqCategories (comcat.h)
description: Registers the class as requiring one or more component categories.
helpviewer_keywords: ["ICatRegister interface [COM]","RegisterClassReqCategories method","ICatRegister.RegisterClassReqCategories","ICatRegister::RegisterClassReqCategories","RegisterClassReqCategories","RegisterClassReqCategories method [COM]","RegisterClassReqCategories method [COM]","ICatRegister interface","_com_icatregister_registerclassreqcategories","com.icatregister_registerclassreqcategories","comcat/ICatRegister::RegisterClassReqCategories"]
old-location: com\icatregister_registerclassreqcategories.htm
tech.root: com
ms.assetid: 56aa5fcd-b46a-4807-ba51-9b4b6d28ceeb
ms.date: 12/05/2018
ms.keywords: ICatRegister interface [COM],RegisterClassReqCategories method, ICatRegister.RegisterClassReqCategories, ICatRegister::RegisterClassReqCategories, RegisterClassReqCategories, RegisterClassReqCategories method [COM], RegisterClassReqCategories method [COM],ICatRegister interface, _com_icatregister_registerclassreqcategories, com.icatregister_registerclassreqcategories, comcat/ICatRegister::RegisterClassReqCategories
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
 - ICatRegister::RegisterClassReqCategories
 - comcat/ICatRegister::RegisterClassReqCategories
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
 - ICatRegister.RegisterClassReqCategories
---

# ICatRegister::RegisterClassReqCategories


## -description

Registers the class as requiring one or more component categories.

## -parameters

### -param rclsid [in]

The class identifier.

### -param cCategories [in]

The number of category CATIDs to be associated as category identifiers for the class.

### -param rgcatid [in]

An array of CATIDs to be associated as category identifiers for the class.

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