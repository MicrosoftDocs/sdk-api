---
UID: NF:comcat.ICatInformation.EnumImplCategoriesOfClass
title: ICatInformation::EnumImplCategoriesOfClass (comcat.h)
description: Retrieves an enumerator for the CATIDs implemented by the specified class.
helpviewer_keywords: ["EnumImplCategoriesOfClass","EnumImplCategoriesOfClass method [COM]","EnumImplCategoriesOfClass method [COM]","ICatInformation interface","ICatInformation interface [COM]","EnumImplCategoriesOfClass method","ICatInformation.EnumImplCategoriesOfClass","ICatInformation::EnumImplCategoriesOfClass","_com_icatinformation_enumimplcategoriesofclass","com.icatinformation_enumimplcategoriesofclass","comcat/ICatInformation::EnumImplCategoriesOfClass"]
old-location: com\icatinformation_enumimplcategoriesofclass.htm
tech.root: com
ms.assetid: 82d938b0-c05d-4bd9-b33f-c7944ed1399b
ms.date: 12/05/2018
ms.keywords: EnumImplCategoriesOfClass, EnumImplCategoriesOfClass method [COM], EnumImplCategoriesOfClass method [COM],ICatInformation interface, ICatInformation interface [COM],EnumImplCategoriesOfClass method, ICatInformation.EnumImplCategoriesOfClass, ICatInformation::EnumImplCategoriesOfClass, _com_icatinformation_enumimplcategoriesofclass, com.icatinformation_enumimplcategoriesofclass, comcat/ICatInformation::EnumImplCategoriesOfClass
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
 - ICatInformation::EnumImplCategoriesOfClass
 - comcat/ICatInformation::EnumImplCategoriesOfClass
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
 - ICatInformation.EnumImplCategoriesOfClass
---

# ICatInformation::EnumImplCategoriesOfClass


## -description

Retrieves an enumerator for the CATIDs implemented by the specified class.

## -parameters

### -param rclsid [in]

The class ID.

### -param ppenumCatid [out]

A pointer to an <a href="/windows/desktop/api/comcat/nn-comcat-ienumguid">IEnumCATID</a> interface pointer. This can be used to enumerate the CATIDs that are implemented by <i>rclsid</i>.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-icatinformation">ICatInformation</a>