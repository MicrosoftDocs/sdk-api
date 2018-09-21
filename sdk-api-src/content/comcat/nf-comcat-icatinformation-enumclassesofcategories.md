---
UID: NF:comcat.ICatInformation.EnumClassesOfCategories
title: ICatInformation::EnumClassesOfCategories
author: windows-sdk-content
description: Retrieves an enumerator for the classes that implement one or more specified category identifiers.
old-location: com\icatinformation_enumclassesofcategories.htm
tech.root: com
ms.assetid: 13d470ff-77e6-4a17-b2c9-c53676e21fba
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: EnumClassesOfCategories, EnumClassesOfCategories method [COM], EnumClassesOfCategories method [COM],ICatInformation interface, ICatInformation interface [COM],EnumClassesOfCategories method, ICatInformation.EnumClassesOfCategories, ICatInformation::EnumClassesOfCategories, _com_icatinformation_enumclassesofcategories, com.icatinformation_enumclassesofcategories, comcat/ICatInformation::EnumClassesOfCategories
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICatInformation.EnumClassesOfCategories
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

A pointer to an <a href="https://msdn.microsoft.com/0b2a39e4-105e-4ba7-bfa4-3ecd75dae4b3">IEnumCLSID</a> interface pointer that can be used to enumerate the CLSIDs of the classes that implement the specified category.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd542655(v=VS.85).aspx">ICatInformation</a>
 

 

