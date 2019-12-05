---
UID: NN:searchapi.ISearchProtocol
title: ISearchProtocol (searchapi.h)
description: Provides methods for invoking, initializing, and managing IUrlAccessor objects.
old-location: search\_search_ISearchProtocol.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol\isearchprotocol.htm
ms.date: 12/05/2018
ms.keywords: ISearchProtocol, ISearchProtocol interface [search], ISearchProtocol interface [search],described, _search_ISearchProtocol, search._search_ISearchProtocol, searchapi/ISearchProtocol
ms.topic: interface
f1_keywords:
- searchapi/ISearchProtocol
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Searchapi.h
api_name:
- ISearchProtocol
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchProtocol interface


## -description


Provides methods for invoking, initializing, and managing <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> objects. Methods in this interface are called by the protocol host when processing URLs from the gatherer. 
        

The protocol handler implements the protocol for accessing a content source in its native format. Use this interface to implement a custom protocol handler to expand the data sources that can be indexed. 
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchProtocol</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchProtocol</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchProtocol</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchprotocol-closeaccessor">CloseAccessor</a>
</td>
<td align="left" width="63%">
Closes a previously created <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchprotocol-createaccessor">CreateAccessor</a>
</td>
<td align="left" width="63%">
Creates and initializes an <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object.  
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchprotocol-init">Init</a>
</td>
<td align="left" width="63%">
Initializes a protocol handler. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchprotocol-shutdown">ShutDown</a>
</td>
<td align="left" width="63%">
Shuts down the protocol handler.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>
 

 

