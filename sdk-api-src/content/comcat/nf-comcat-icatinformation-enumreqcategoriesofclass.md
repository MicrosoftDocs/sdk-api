---
UID: NF:comcat.ICatInformation.EnumReqCategoriesOfClass
title: ICatInformation::EnumReqCategoriesOfClass
author: windows-sdk-content
description: Retrieves an enumerator for the CATIDs required by the specified class.
old-location: com\icatinformation_enumreqcategoriesofclass.htm
tech.root: com
ms.assetid: 1bde9359-6d0e-4d8f-9c9b-ceabaf2da61f
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: EnumReqCategoriesOfClass, EnumReqCategoriesOfClass method [COM], EnumReqCategoriesOfClass method [COM],ICatInformation interface, ICatInformation interface [COM],EnumReqCategoriesOfClass method, ICatInformation.EnumReqCategoriesOfClass, ICatInformation::EnumReqCategoriesOfClass, _com_icatinformation_enumreqcategoriesofclass, com.icatinformation_enumreqcategoriesofclass, comcat/ICatInformation::EnumReqCategoriesOfClass
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
 - ICatInformation.EnumReqCategoriesOfClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICatInformation::EnumReqCategoriesOfClass


## -description


Retrieves an enumerator for the CATIDs required by the specified class.


## -parameters




### -param rclsid [in]

The class identifier.


### -param ppenumCatid [out]

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms682393(v=VS.85).aspx">IEnumCATID</a> interface pointer. This can be used to enumerate the CATIDs that are required by <i>rclsid</i>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd542655(v=VS.85).aspx">ICatInformation</a>
 

 

