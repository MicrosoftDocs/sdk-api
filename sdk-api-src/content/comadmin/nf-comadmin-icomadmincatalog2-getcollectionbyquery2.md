---
UID: NF:comadmin.ICOMAdminCatalog2.GetCollectionByQuery2
title: ICOMAdminCatalog2::GetCollectionByQuery2
author: windows-sdk-content
description: Retrieves a collection of items in the COM+ catalog that satisfy the specified set of query keys.
old-location: cos\icomadmincatalog2_getcollectionbyquery2.htm
tech.root: cossdk
ms.assetid: b1861e8f-bb42-42b5-9435-6fa366f8284a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetCollectionByQuery2, GetCollectionByQuery2 method [COM+], GetCollectionByQuery2 method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],GetCollectionByQuery2 method, ICOMAdminCatalog2.GetCollectionByQuery2, ICOMAdminCatalog2::GetCollectionByQuery2, _cos_icomadmincatalog2_GetCollectionByQuery2, comadmin/ICOMAdminCatalog2::GetCollectionByQuery2, cos.icomadmincatalog2_getcollectionbyquery2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.GetCollectionByQuery2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICOMAdminCatalog2::GetCollectionByQuery2


## -description


Retrieves a collection of items in the COM+ catalog that satisfy the specified set of query keys.


## -parameters




### -param bstrCollectionName [in]

The name of the collection to be retrieved from the catalog. Possible collection names can be found in the table of collections at <a href="https://msdn.microsoft.com/eed8ca97-39ad-4188-afc6-8670b5073fad">COM+ Administration Collections</a>.


### -param pVarQueryStrings [in]

The query keys.


### -param ppCatalogCollection [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/7c24ead4-d69f-467d-b3d8-a81adbc49a7b">ICatalogCollection</a> interface pointer containing the result of the query.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/ffca611d-dacc-47be-9101-9de76ecc8393">ICOMAdminCatalog2</a>
 

 

