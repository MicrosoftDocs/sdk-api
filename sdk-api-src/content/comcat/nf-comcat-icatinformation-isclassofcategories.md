---
UID: NF:comcat.ICatInformation.IsClassOfCategories
title: ICatInformation::IsClassOfCategories
author: windows-driver-content
description: Determines whether a class implements one or more categories.
old-location: com\icatinformation_isclassofcategories.htm
old-project: com
ms.assetid: 772d4d75-2076-4922-bf47-2e6e41a5687d
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ICatInformation interface [COM],IsClassOfCategories method, ICatInformation.IsClassOfCategories, ICatInformation::IsClassOfCategories, IsClassOfCategories, IsClassOfCategories method [COM], IsClassOfCategories method [COM],ICatInformation interface, _com_icatinformation_isclassofcategories, com.icatinformation_isclassofcategories, comcat/ICatInformation::IsClassOfCategories
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
req.typenames: ServerInformation, *PServerInformation
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComCat.h
api_name:
-	ICatInformation.IsClassOfCategories
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatInformation::IsClassOfCategories


## -description


Determines whether a class implements one or more categories.


## -parameters




### -param rclsid [in]

The class identifier.


### -param cImplemented [in]

The number of category IDs in the <i>rgcatidImpl</i> array. This value cannot be zero. If this value is -1, the implemented categories are not tested.


### -param rgcatidImpl [in]

An array of category identifiers.

If the class requires a category not listed in <i>rgcatidReq</i>, it is not included in the enumeration.



### -param cRequired [in]

The number of category IDs in the <i>rgcatidReq</i> array. This value can be zero. If this value is -1, the required categories are not tested.


### -param rgcatidReq [in]

An array of category identifiers.


## -returns



If the class ID is of one of the specified categories, the return value is S_OK. Otherwise, is it S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/1fd68126-b512-4131-8e93-cea7c1c3e9c0">ICatInformation</a>
 

 

