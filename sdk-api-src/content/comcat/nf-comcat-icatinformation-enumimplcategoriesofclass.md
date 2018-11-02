---
UID: NF:comcat.ICatInformation.EnumImplCategoriesOfClass
title: ICatInformation::EnumImplCategoriesOfClass
author: windows-sdk-content
description: Retrieves an enumerator for the CATIDs implemented by the specified class.
old-location: com\icatinformation_enumimplcategoriesofclass.htm
tech.root: com
ms.assetid: 82d938b0-c05d-4bd9-b33f-c7944ed1399b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EnumImplCategoriesOfClass, EnumImplCategoriesOfClass method [COM], EnumImplCategoriesOfClass method [COM],ICatInformation interface, ICatInformation interface [COM],EnumImplCategoriesOfClass method, ICatInformation.EnumImplCategoriesOfClass, ICatInformation::EnumImplCategoriesOfClass, _com_icatinformation_enumimplcategoriesofclass, com.icatinformation_enumimplcategoriesofclass, comcat/ICatInformation::EnumImplCategoriesOfClass
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
 - ICatInformation.EnumImplCategoriesOfClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICatInformation::EnumImplCategoriesOfClass


## -description


Retrieves an enumerator for the CATIDs implemented by the specified class.


## -parameters




### -param rclsid [in]

The class ID.


### -param ppenumCatid [out]

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms682393(v=VS.85).aspx">IEnumCATID</a> interface pointer. This can be used to enumerate the CATIDs that are implemented by <i>rclsid</i>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd542655(v=VS.85).aspx">ICatInformation</a>
 

 

