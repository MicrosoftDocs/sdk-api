---
UID: NF:comadmin.ICatalogCollection.Add
title: ICatalogCollection::Add (comadmin.h)
description: Adds an item to the collection, giving it the high index value.
helpviewer_keywords: ["Add","Add method [COM+]","Add method [COM+]","ICatalogCollection interface","ICatalogCollection interface [COM+]","Add method","ICatalogCollection.Add","ICatalogCollection::Add","_cos_ICatalogCollection_Add","comadmin/ICatalogCollection::Add","cos.icatalogcollection_add"]
old-location: cos\icatalogcollection_add.htm
tech.root: cos
ms.assetid: 0826a2f0-d4a5-40e2-b951-291d67f0d201
ms.date: 12/05/2018
ms.keywords: Add, Add method [COM+], Add method [COM+],ICatalogCollection interface, ICatalogCollection interface [COM+],Add method, ICatalogCollection.Add, ICatalogCollection::Add, _cos_ICatalogCollection_Add, comadmin/ICatalogCollection::Add, cos.icatalogcollection_add
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
 - ICatalogCollection::Add
 - comadmin/ICatalogCollection::Add
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
 - ICatalogCollection.Add
---

# ICatalogCollection::Add


## -description

Adds an item to the collection, giving it the high index value.

## -parameters

### -param ppCatalogObject [out, retval]

A pointer to the <a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogobject">ICatalogObject</a> interface pointer for the new object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

The <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_addenabled">AddEnabled</a> property indicates whether the collection supports this method.

When an object is added, the <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_count">Count</a> property is incremented to reflect the change.

This change is not reflected in the persisted COM+ catalog data store until you use <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-savechanges">SaveChanges</a>.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogcollection">ICatalogCollection</a>