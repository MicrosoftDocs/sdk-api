---
UID: NF:comcat.ICatInformation.EnumReqCategoriesOfClass
title: ICatInformation::EnumReqCategoriesOfClass (comcat.h)
author: windows-sdk-content
description: Retrieves an enumerator for the CATIDs required by the specified class.
old-location: com\icatinformation_enumreqcategoriesofclass.htm
tech.root: com
ms.assetid: 1bde9359-6d0e-4d8f-9c9b-ceabaf2da61f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumReqCategoriesOfClass, EnumReqCategoriesOfClass method [COM], EnumReqCategoriesOfClass method [COM],ICatInformation interface, ICatInformation interface [COM],EnumReqCategoriesOfClass method, ICatInformation.EnumReqCategoriesOfClass, ICatInformation::EnumReqCategoriesOfClass, _com_icatinformation_enumreqcategoriesofclass, com.icatinformation_enumreqcategoriesofclass, comcat/ICatInformation::EnumReqCategoriesOfClass
ms.topic: method
f1_keywords: 
 - "comcat/ICatInformation.EnumReqCategoriesOfClass"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICatInformation::EnumReqCategoriesOfClass


## -description


Retrieves an enumerator for the CATIDs required by the specified class.


## -parameters




### -param rclsid [in]

The class identifier.


### -param ppenumCatid [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/comcat/nn-comcat-ienumguid">IEnumCATID</a> interface pointer. This can be used to enumerate the CATIDs that are required by <i>rclsid</i>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comcat/nn-comcat-icatinformation">ICatInformation</a>
 

 

