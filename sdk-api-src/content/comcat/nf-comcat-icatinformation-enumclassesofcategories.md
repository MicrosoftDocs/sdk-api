---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/1fd68126-b512-4131-8e93-cea7c1c3e9c0">ICatInformation</a>
 

 

