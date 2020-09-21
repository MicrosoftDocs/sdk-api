---
UID: NF:comadmin.ICOMAdminCatalog.GetCollectionByQuery
title: ICOMAdminCatalog::GetCollectionByQuery (comadmin.h)
description: Retrieves a collection on the COM+ catalog given the key property values for all of its parent items.
helpviewer_keywords: ["GetCollectionByQuery","GetCollectionByQuery method [COM+]","GetCollectionByQuery method [COM+]","ICOMAdminCatalog interface","ICOMAdminCatalog interface [COM+]","GetCollectionByQuery method","ICOMAdminCatalog.GetCollectionByQuery","ICOMAdminCatalog::GetCollectionByQuery","_cos_ICOMAdminCatalog_GetCollectionByQuery","comadmin/ICOMAdminCatalog::GetCollectionByQuery","cos.icomadmincatalog_getcollectionbyquery"]
old-location: cos\icomadmincatalog_getcollectionbyquery.htm
tech.root: cos
ms.assetid: 6ec65e7c-fb67-4435-90cd-d17b8fbcbc84
ms.date: 12/05/2018
ms.keywords: GetCollectionByQuery, GetCollectionByQuery method [COM+], GetCollectionByQuery method [COM+],ICOMAdminCatalog interface, ICOMAdminCatalog interface [COM+],GetCollectionByQuery method, ICOMAdminCatalog.GetCollectionByQuery, ICOMAdminCatalog::GetCollectionByQuery, _cos_ICOMAdminCatalog_GetCollectionByQuery, comadmin/ICOMAdminCatalog::GetCollectionByQuery, cos.icomadmincatalog_getcollectionbyquery
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
 - ICOMAdminCatalog::GetCollectionByQuery
 - comadmin/ICOMAdminCatalog::GetCollectionByQuery
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
 - ICOMAdminCatalog.GetCollectionByQuery
---

# ICOMAdminCatalog::GetCollectionByQuery


## -description

Retrieves a collection on the COM+ catalog given the key property values for all of its parent items.

## -parameters

### -param bstrCollName [in]

The name of the collection to be retrieved.

### -param ppsaVarQuery [in]

A reference to an array consisting of key property values for all parent items of the collection to be retrieved.

### -param ppCatalogCollection [out, retval]

The <a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogcollection">ICatalogCollection</a> interface for the collection.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

The <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-get_key">ICatalogObject::Key</a> property value for an item is a GUID that serves to uniquely identify it in the COM+ catalog.

The <b>GetCollectionByQuery</b> method retrieves any collection on the catalog, given the key values for all of its parent items. However, with the <a href="/windows/desktop/cossdk/errorinfo">ErrorInfo</a>, <a href="/windows/desktop/cossdk/propertyinfo">PropertyInfo</a>, and <a href="/windows/desktop/cossdk/relatedcollectioninfo">RelatedCollectionInfo</a> collections, this method behaves differently. If you specify any of these collections, <b>GetCollectionByQuery</b> always returns that named collection immediately relative to the <a href="/windows/desktop/cossdk/root">Root</a> collection.

To get the <a href="/windows/desktop/cossdk/errorinfo">ErrorInfo</a>, <a href="/windows/desktop/cossdk/propertyinfo">PropertyInfo</a>, or <a href="/windows/desktop/cossdk/relatedcollectioninfo">RelatedCollectionInfo</a> collection that is relative to an arbitrary collection in the catalog and not relative to the <a href="/windows/desktop/cossdk/root">Root</a> collection, use the <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-getcollection">GetCollection</a> method from the parent collection.

For a complete list of available collections, see <a href="/windows/desktop/cossdk/com--administration-collections">COM+ Administration Collections</a>.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>