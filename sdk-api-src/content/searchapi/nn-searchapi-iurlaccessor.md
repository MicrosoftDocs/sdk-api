---
UID: NN:searchapi.IUrlAccessor
title: IUrlAccessor (searchapi.h)
description: Provides methods for processing an individual item in a content source whose URL is provided by the gatherer to the filter host.
helpviewer_keywords: ["IUrlAccessor","IUrlAccessor interface [search]","IUrlAccessor interface [search]","described","_search_IUrlAccessor","search._search_IUrlAccessor","searchapi/IUrlAccessor"]
old-location: search\_search_IUrlAccessor.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\iurlaccessor.htm
ms.date: 12/05/2018
ms.keywords: IUrlAccessor, IUrlAccessor interface [search], IUrlAccessor interface [search],described, _search_IUrlAccessor, search._search_IUrlAccessor, searchapi/IUrlAccessor
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Urlaccsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IUrlAccessor
 - searchapi/IUrlAccessor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - IUrlAccessor
---

# IUrlAccessor interface


## -description

Provides methods for processing an individual item in a content source whose URL is provided by the gatherer to the filter host.

## -inheritance

The <b>IUrlAccessor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUrlAccessor</b> also has these types of members:

## -remarks

This is the main interface for pulling data from the content source. The Get... methods are for properties that are required by or useful to the filter host. Not all data sources have these properties. If the property returned by one of these methods is not meaningful for your data source, your protocol handler should return E_NOTIMPL.

The Bind... methods provide access to the data.

Although the protocol handler runs in the protocol host's multithreaded environment, each protocol handler runs in its own thread, employing one <b>IUrlAccessor</b> object at a time.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor2">IUrlAccessor2</a>



<a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor3">IUrlAccessor3</a>



<b>Reference</b>



<a href="/windows/desktop/search/-search-prth-error-constants">Search Protocol Handler Error Messages</a>



<a href="/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>
