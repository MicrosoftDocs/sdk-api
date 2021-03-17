---
UID: NF:comadmin.ICOMAdminCatalog2.GetCollectionByQuery2
title: ICOMAdminCatalog2::GetCollectionByQuery2 (comadmin.h)
description: Retrieves a collection of items in the COM+ catalog that satisfy the specified set of query keys.
helpviewer_keywords: ["GetCollectionByQuery2","GetCollectionByQuery2 method [COM+]","GetCollectionByQuery2 method [COM+]","ICOMAdminCatalog2 interface","ICOMAdminCatalog2 interface [COM+]","GetCollectionByQuery2 method","ICOMAdminCatalog2.GetCollectionByQuery2","ICOMAdminCatalog2::GetCollectionByQuery2","_cos_icomadmincatalog2_GetCollectionByQuery2","comadmin/ICOMAdminCatalog2::GetCollectionByQuery2","cos.icomadmincatalog2_getcollectionbyquery2"]
old-location: cos\icomadmincatalog2_getcollectionbyquery2.htm
tech.root: cos
ms.assetid: b1861e8f-bb42-42b5-9435-6fa366f8284a
ms.date: 12/05/2018
ms.keywords: GetCollectionByQuery2, GetCollectionByQuery2 method [COM+], GetCollectionByQuery2 method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],GetCollectionByQuery2 method, ICOMAdminCatalog2.GetCollectionByQuery2, ICOMAdminCatalog2::GetCollectionByQuery2, _cos_icomadmincatalog2_GetCollectionByQuery2, comadmin/ICOMAdminCatalog2::GetCollectionByQuery2, cos.icomadmincatalog2_getcollectionbyquery2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICOMAdminCatalog2::GetCollectionByQuery2
 - comadmin/ICOMAdminCatalog2::GetCollectionByQuery2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.GetCollectionByQuery2
---

# ICOMAdminCatalog2::GetCollectionByQuery2


## -description

Retrieves a collection of items in the COM+ catalog that satisfy the specified set of query keys.

## -parameters

### -param bstrCollectionName [in]

The name of the collection to be retrieved from the catalog. Possible collection names can be found in the table of collections at <a href="/windows/desktop/cossdk/com--administration-collections">COM+ Administration Collections</a>.

### -param pVarQueryStrings [in]

The query keys.

### -param ppCatalogCollection [out, retval]

A pointer to an <a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogcollection">ICatalogCollection</a> interface pointer containing the result of the query.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>