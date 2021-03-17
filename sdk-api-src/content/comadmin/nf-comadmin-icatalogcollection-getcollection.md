---
UID: NF:comadmin.ICatalogCollection.GetCollection
title: ICatalogCollection::GetCollection (comadmin.h)
description: Retrieves a collection from the COM+ catalog that is related to the current collection.
helpviewer_keywords: ["GetCollection","GetCollection method [COM+]","GetCollection method [COM+]","ICatalogCollection interface","ICatalogCollection interface [COM+]","GetCollection method","ICatalogCollection.GetCollection","ICatalogCollection::GetCollection","_cos_ICatalogCollection_GetCollection","comadmin/ICatalogCollection::GetCollection","cos.icatalogcollection_getcollection"]
old-location: cos\icatalogcollection_getcollection.htm
tech.root: cos
ms.assetid: 4198f456-97fa-45b2-aa79-29ac506a8618
ms.date: 12/05/2018
ms.keywords: GetCollection, GetCollection method [COM+], GetCollection method [COM+],ICatalogCollection interface, ICatalogCollection interface [COM+],GetCollection method, ICatalogCollection.GetCollection, ICatalogCollection::GetCollection, _cos_ICatalogCollection_GetCollection, comadmin/ICatalogCollection::GetCollection, cos.icatalogcollection_getcollection
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ICatalogCollection::GetCollection
 - comadmin/ICatalogCollection::GetCollection
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
 - ICatalogCollection.GetCollection
---

# ICatalogCollection::GetCollection


## -description

Retrieves a collection from the COM+ catalog that is related to the current collection.

## -parameters

### -param bstrCollName [in]

The name of the collection to be retrieved.

### -param varObjectKey [in]

The <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-get_key">Key</a> property value of the parent item of the collection to be retrieved.

### -param ppCatalogCollection [out, retval]

The <a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogcollection">ICatalogCollection</a> interface for the retrieved collection.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

This method does not read in data for items in the retrieved collection from the catalog data store. Use the <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-populate">Populate</a> method to read in data for items in the collection.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogcollection">ICatalogCollection</a>