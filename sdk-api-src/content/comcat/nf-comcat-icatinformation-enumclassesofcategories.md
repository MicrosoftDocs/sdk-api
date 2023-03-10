---
UID: NF:comcat.ICatInformation.EnumClassesOfCategories
title: ICatInformation::EnumClassesOfCategories (comcat.h)
description: Retrieves an enumerator for the classes that implement one or more specified category identifiers.
helpviewer_keywords: ["EnumClassesOfCategories","EnumClassesOfCategories method [COM]","EnumClassesOfCategories method [COM]","ICatInformation interface","ICatInformation interface [COM]","EnumClassesOfCategories method","ICatInformation.EnumClassesOfCategories","ICatInformation::EnumClassesOfCategories","_com_icatinformation_enumclassesofcategories","com.icatinformation_enumclassesofcategories","comcat/ICatInformation::EnumClassesOfCategories"]
old-location: com\icatinformation_enumclassesofcategories.htm
tech.root: com
ms.assetid: 13d470ff-77e6-4a17-b2c9-c53676e21fba
ms.date: 12/05/2018
ms.keywords: EnumClassesOfCategories, EnumClassesOfCategories method [COM], EnumClassesOfCategories method [COM],ICatInformation interface, ICatInformation interface [COM],EnumClassesOfCategories method, ICatInformation.EnumClassesOfCategories, ICatInformation::EnumClassesOfCategories, _com_icatinformation_enumclassesofcategories, com.icatinformation_enumclassesofcategories, comcat/ICatInformation::EnumClassesOfCategories
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
 - ICatInformation::EnumClassesOfCategories
 - comcat/ICatInformation::EnumClassesOfCategories
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
 - ICatInformation.EnumClassesOfCategories
---

# ICatInformation::EnumClassesOfCategories


## -description

Retrieves an enumerator for the classes that implement one or more specified category identifiers.

## -parameters

### -param cImplemented [in]

The number of category IDs in the <i>rgcatidImpl</i> array. This value cannot be zero. If this value is -1, classes are included in the enumeration, regardless of the categories they implement.

### -param rgcatidImpl [in]

An array of category identifiers.

If a class requires a category identifier that is not specified, it is not included in the enumeration.

### -param cRequired [in]

The number of category IDs in the <i>rgcatidReq</i> array. This value can be zero. If this value is -1, classes are included in the enumeration, regardless of the categories they require.

### -param rgcatidReq [in]

An array of category identifiers.

### -param ppenumClsid [out]

A pointer to an <a href="/previous-versions/windows/desktop/legacy/dd542667(v=vs.85)">IEnumCLSID</a> interface pointer that can be used to enumerate the CLSIDs of the classes that implement the specified category.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-icatinformation">ICatInformation</a>