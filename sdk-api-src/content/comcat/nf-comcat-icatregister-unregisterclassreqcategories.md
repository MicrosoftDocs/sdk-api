---
UID: NF:comcat.ICatRegister.UnRegisterClassReqCategories
title: ICatRegister::UnRegisterClassReqCategories (comcat.h)
description: Removes one or more required category identifiers from a class.
helpviewer_keywords: ["ICatRegister interface [COM]","UnRegisterClassReqCategories method","ICatRegister.UnRegisterClassReqCategories","ICatRegister::UnRegisterClassReqCategories","UnRegisterClassReqCategories","UnRegisterClassReqCategories method [COM]","UnRegisterClassReqCategories method [COM]","ICatRegister interface","_com_icatregister_unregisterclassreqcategories","com.icatregister_unregisterclassreqcategories","comcat/ICatRegister::UnRegisterClassReqCategories"]
old-location: com\icatregister_unregisterclassreqcategories.htm
tech.root: com
ms.assetid: d957bc13-f5f7-4cb3-925e-4867ba9622cd
ms.date: 12/05/2018
ms.keywords: ICatRegister interface [COM],UnRegisterClassReqCategories method, ICatRegister.UnRegisterClassReqCategories, ICatRegister::UnRegisterClassReqCategories, UnRegisterClassReqCategories, UnRegisterClassReqCategories method [COM], UnRegisterClassReqCategories method [COM],ICatRegister interface, _com_icatregister_unregisterclassreqcategories, com.icatregister_unregisterclassreqcategories, comcat/ICatRegister::UnRegisterClassReqCategories
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
 - ICatRegister::UnRegisterClassReqCategories
 - comcat/ICatRegister::UnRegisterClassReqCategories
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
 - ICatRegister.UnRegisterClassReqCategories
---

# ICatRegister::UnRegisterClassReqCategories


## -description

Removes one or more required category identifiers from a class.

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

In case of an error, this method does not ensure that the registry is restored to the state prior to the call. This method will be successful even if one or more of the category IDs specified are not registered for the class.

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-icatregister">ICatRegister</a>