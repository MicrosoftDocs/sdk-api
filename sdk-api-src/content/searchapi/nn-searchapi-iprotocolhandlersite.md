---
UID: NN:searchapi.IProtocolHandlerSite
title: IProtocolHandlerSite
author: windows-sdk-content
description: Provides methods for a protocol handler's IUrlAccessor object to query the Filter Daemon for the appropriate filter for the URL item.
old-location: search\_search_IProtocolHandlerSite.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iprotocolhandlersite\iprotocolhandlersite.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IProtocolHandlerSite, IProtocolHandlerSite interface [search], IProtocolHandlerSite interface [search],described, _search_IProtocolHandlerSite, search._search_IProtocolHandlerSite, searchapi/IProtocolHandlerSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - IProtocolHandlerSite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IProtocolHandlerSite interface


## -description


Provides methods for a protocol handler's <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object to query the Filter Daemon for the appropriate filter for the URL item.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProtocolHandlerSite</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProtocolHandlerSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProtocolHandlerSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e033abd2-864f-406f-a933-fe80038f1943">GetFilter</a>
</td>
<td align="left" width="63%">

        Retrieves the appropriate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>according to the supplied parameters.     
        

</td>
</tr>
</table> 


## -remarks



When a protocol handler encounters items with embedded documents, the protocol handler requests additional filters from the Filter Daemon by calling the <a href="search._search_IProtocolHandlerSite_GetFilter">IProtocolHandlerSite::GetFilter</a> method.




## -see-also




<a href="https://msdn.microsoft.com/cfba12eb-4123-4b57-8311-d4fc8f9f514e">The Indexing Process</a>
 

 

