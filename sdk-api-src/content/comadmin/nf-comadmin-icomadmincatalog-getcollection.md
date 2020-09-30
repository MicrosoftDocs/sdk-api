---
UID: NF:comadmin.ICOMAdminCatalog.GetCollection
title: ICOMAdminCatalog::GetCollection (comadmin.h)
description: Retrieves a top-level collection on the COM+ catalog.
helpviewer_keywords: ["GetCollection","GetCollection method [COM+]","GetCollection method [COM+]","ICOMAdminCatalog interface","ICOMAdminCatalog interface [COM+]","GetCollection method","ICOMAdminCatalog.GetCollection","ICOMAdminCatalog::GetCollection","_cos_ICOMAdminCatalog_GetCollection","comadmin/ICOMAdminCatalog::GetCollection","cos.icomadmincatalog_getcollection"]
old-location: cos\icomadmincatalog_getcollection.htm
tech.root: cos
ms.assetid: 6f01a7a7-d8f3-470f-8eb3-aa698b353af1
ms.date: 12/05/2018
ms.keywords: GetCollection, GetCollection method [COM+], GetCollection method [COM+],ICOMAdminCatalog interface, ICOMAdminCatalog interface [COM+],GetCollection method, ICOMAdminCatalog.GetCollection, ICOMAdminCatalog::GetCollection, _cos_ICOMAdminCatalog_GetCollection, comadmin/ICOMAdminCatalog::GetCollection, cos.icomadmincatalog_getcollection
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
 - ICOMAdminCatalog::GetCollection
 - comadmin/ICOMAdminCatalog::GetCollection
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
 - ICOMAdminCatalog.GetCollection
---

# ICOMAdminCatalog::GetCollection


## -description

Retrieves a top-level collection on the COM+ catalog.

## -parameters

### -param bstrCollName [in]

The name of the collection to be retrieved.

### -param ppCatalogCollection [out, retval]

The <a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogcollection">ICatalogCollection</a> interface for the collection.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

This method retrieves a top-level collection, such as the <a href="/windows/desktop/cossdk/applications">Applications</a> collection, from the COM+ catalog. For related collections that are not top-level collections, such as <a href="/windows/desktop/cossdk/components">Components</a>, use the <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-getcollection">GetCollection</a> method available from the parent collection.

The catalog collection retrieved by <b>GetCollection</b> does not contain data from the catalog for items contained within the collection. Use the <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-populate">Populate</a> method to read in data for items in the collection.

For a complete list of collections in the COM+ catalog, see <a href="/windows/desktop/cossdk/com--administration-collections">COM+ Administration Collections</a>.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>