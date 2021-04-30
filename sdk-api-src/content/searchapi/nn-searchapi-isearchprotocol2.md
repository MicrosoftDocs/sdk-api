---
UID: NN:searchapi.ISearchProtocol2
title: ISearchProtocol2 (searchapi.h)
description: Provides methods for invoking, initializing, and managing IUrlAccessor objects.
helpviewer_keywords: ["ISearchProtocol2","ISearchProtocol2 interface [search]","ISearchProtocol2 interface [search]","described","_search_ISearchProtocol2","search._search_ISearchProtocol2","searchapi/ISearchProtocol2"]
old-location: search\_search_ISearchProtocol2.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol2\isearchprotocol2.htm
ms.date: 12/05/2018
ms.keywords: ISearchProtocol2, ISearchProtocol2 interface [search], ISearchProtocol2 interface [search],described, _search_ISearchProtocol2, search._search_ISearchProtocol2, searchapi/ISearchProtocol2
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ISearchProtocol2
 - searchapi/ISearchProtocol2
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
 - ISearchProtocol2
---

# ISearchProtocol2 interface


## -description

Provides methods for invoking, initializing, and managing <a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> objects. Methods in this interface are called by the protocol host when processing URLs from the gatherer. 
      
The protocol handler implements the protocol for accessing a content source in its native format. Use this interface to implement a custom protocol handler to expand the data sources that can be indexed.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchProtocol2</b> interface inherits from <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol">ISearchProtocol</a>. <b>ISearchProtocol2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol">ISearchProtocol</a>



<a href="/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>
