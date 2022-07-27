---
UID: NN:searchapi.ISearchProtocol
title: ISearchProtocol (searchapi.h)
description: Provides methods for invoking, initializing, and managing IUrlAccessor objects. (ISearchProtocol)
helpviewer_keywords: ["ISearchProtocol","ISearchProtocol interface [search]","ISearchProtocol interface [search]","described","_search_ISearchProtocol","search._search_ISearchProtocol","searchapi/ISearchProtocol"]
old-location: search\_search_ISearchProtocol.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol\isearchprotocol.htm
ms.date: 12/05/2018
ms.keywords: ISearchProtocol, ISearchProtocol interface [search], ISearchProtocol interface [search],described, _search_ISearchProtocol, search._search_ISearchProtocol, searchapi/ISearchProtocol
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchprth.idl
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
 - ISearchProtocol
 - searchapi/ISearchProtocol
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
 - ISearchProtocol
---

# ISearchProtocol interface


## -description

Provides methods for invoking, initializing, and managing <a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> objects. Methods in this interface are called by the protocol host when processing URLs from the gatherer. 
        

The protocol handler implements the protocol for accessing a content source in its native format. Use this interface to implement a custom protocol handler to expand the data sources that can be indexed.

## -inheritance

The <b>ISearchProtocol</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchProtocol</b> also has these types of members:

## -see-also

<a href="/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>
