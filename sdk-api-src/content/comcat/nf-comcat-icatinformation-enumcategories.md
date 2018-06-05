---
UID: NF:comcat.ICatInformation.EnumCategories
title: ICatInformation::EnumCategories
author: windows-sdk-content
description: Retrieves an enumerator for the component categories registered on the system.
old-location: com\icatinformation_enumcategories.htm
old-project: com
ms.assetid: d8e744f0-6e50-4260-89df-e2cc59937398
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: EnumCategories, EnumCategories method [COM], EnumCategories method [COM],ICatInformation interface, ICatInformation interface [COM],EnumCategories method, ICatInformation.EnumCategories, ICatInformation::EnumCategories, _com_icatinformation_enumcategories, com.icatinformation_enumcategories, comcat/ICatInformation::EnumCategories
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ServerInformation, *PServerInformation
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComCat.h
api_name:
-	ICatInformation.EnumCategories
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatInformation::EnumCategories


## -description


Retrieves an enumerator for the component categories registered on the system.


## -parameters




### -param lcid [in]

The requested locale for any return szDescription of the enumerated categories. Typically, the caller specifies the value returned from the <a href="https://msdn.microsoft.com/bbf8399e-9034-4480-8d6e-030714f94e48">GetUserDefaultLCID</a> function.


### -param ppenumCategoryInfo [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/87469ace-ae34-40e5-aab6-f26a4bc50b54">IEnumCATEGORYINFO</a> interface. This can be used to enumerate the CATIDs and localized description strings of the component categories registered with the system.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/1fd68126-b512-4131-8e93-cea7c1c3e9c0">ICatInformation</a>
 

 

