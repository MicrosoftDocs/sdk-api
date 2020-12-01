---
UID: NF:comcat.ICatRegister.UnRegisterClassImplCategories
title: ICatRegister::UnRegisterClassImplCategories (comcat.h)
description: Removes one or more implemented category identifiers from a class.
helpviewer_keywords: ["ICatRegister interface [COM]","UnRegisterClassImplCategories method","ICatRegister.UnRegisterClassImplCategories","ICatRegister::UnRegisterClassImplCategories","UnRegisterClassImplCategories","UnRegisterClassImplCategories method [COM]","UnRegisterClassImplCategories method [COM]","ICatRegister interface","_com_icatregister_unregisterclassimplcategories","com.icatregister_unregisterclassimplcategories","comcat/ICatRegister::UnRegisterClassImplCategories"]
old-location: com\icatregister_unregisterclassimplcategories.htm
tech.root: com
ms.assetid: 4a227fd1-6cbc-4354-a3e2-04aceb73ab65
ms.date: 12/05/2018
ms.keywords: ICatRegister interface [COM],UnRegisterClassImplCategories method, ICatRegister.UnRegisterClassImplCategories, ICatRegister::UnRegisterClassImplCategories, UnRegisterClassImplCategories, UnRegisterClassImplCategories method [COM], UnRegisterClassImplCategories method [COM],ICatRegister interface, _com_icatregister_unregisterclassimplcategories, com.icatregister_unregisterclassimplcategories, comcat/ICatRegister::UnRegisterClassImplCategories
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
 - ICatRegister::UnRegisterClassImplCategories
 - comcat/ICatRegister::UnRegisterClassImplCategories
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
 - ICatRegister.UnRegisterClassImplCategories
---

# ICatRegister::UnRegisterClassImplCategories


## -description

Removes one or more implemented category identifiers from a class.

## -parameters

### -param rclsid [in]

The class identifier.

### -param cCategories [in]

The number of category CATIDs to be removed.

### -param rgcatid [in]

An array of CATIDs that are to be removed. Only the category IDs specified in this array are removed.

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

In case of an error, this method does not ensure that the registry is restored to the state prior to the call. This method will be successful even if one or more of the category IDs specified are not registered for the class. This method can only be called by the owner of a class, usually as part of the de-installation of the component.

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-icatregister">ICatRegister</a>