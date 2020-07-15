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
f1_keywords:
- searchapi/ISearchProtocol2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Searchapi.h
api_name:
- ISearchProtocol2
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchProtocol2 interface


## -description


Provides methods for invoking, initializing, and managing <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> objects. Methods in this interface are called by the protocol host when processing URLs from the gatherer. 
      

 
      The protocol handler implements the protocol for accessing a content source in its native format. Use this interface to implement a custom protocol handler to expand the data sources that can be indexed. 
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchProtocol2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol">ISearchProtocol</a>. <b>ISearchProtocol2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchProtocol2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchprotocol2-createaccessorex">CreateAccessorEx</a>
</td>
<td align="left" width="63%">
 
        Creates and initializes an <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object. This method has the same basic functionality as the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchprotocol-createaccessor">ISearchProtocol::CreateAccessor</a> method, but it includes an additional <b>pUserData</b> parameter to supply additional data to the protocol handler.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol">ISearchProtocol</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>
 

 

