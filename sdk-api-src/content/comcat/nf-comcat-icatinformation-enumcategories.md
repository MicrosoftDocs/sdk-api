---
UID: NF:comcat.ICatInformation.EnumCategories
title: ICatInformation::EnumCategories (comcat.h)
description: Retrieves an enumerator for the component categories registered on the system.
helpviewer_keywords: ["EnumCategories","EnumCategories method [COM]","EnumCategories method [COM]","ICatInformation interface","ICatInformation interface [COM]","EnumCategories method","ICatInformation.EnumCategories","ICatInformation::EnumCategories","_com_icatinformation_enumcategories","com.icatinformation_enumcategories","comcat/ICatInformation::EnumCategories"]
old-location: com\icatinformation_enumcategories.htm
tech.root: com
ms.assetid: d8e744f0-6e50-4260-89df-e2cc59937398
ms.date: 12/05/2018
ms.keywords: EnumCategories, EnumCategories method [COM], EnumCategories method [COM],ICatInformation interface, ICatInformation interface [COM],EnumCategories method, ICatInformation.EnumCategories, ICatInformation::EnumCategories, _com_icatinformation_enumcategories, com.icatinformation_enumcategories, comcat/ICatInformation::EnumCategories
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
 - ICatInformation::EnumCategories
 - comcat/ICatInformation::EnumCategories
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
 - ICatInformation.EnumCategories
---

# ICatInformation::EnumCategories


## -description

Retrieves an enumerator for the component categories registered on the system.

## -parameters

### -param lcid [in]

The requested locale for any return szDescription of the enumerated categories. Typically, the caller specifies the value returned from the <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlcid">GetUserDefaultLCID</a> function.

### -param ppenumCategoryInfo [out]

A pointer to a pointer to an <a href="/windows/desktop/api/comcat/nn-comcat-ienumcategoryinfo">IEnumCATEGORYINFO</a> interface. This can be used to enumerate the CATIDs and localized description strings of the component categories registered with the system.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-icatinformation">ICatInformation</a>