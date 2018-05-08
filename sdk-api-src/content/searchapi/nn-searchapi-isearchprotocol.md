---
UID: NN:searchapi.ISearchProtocol
title: ISearchProtocol
author: windows-driver-content
description: Provides methods for invoking, initializing, and managing IUrlAccessor objects.
old-location: search\_search_ISearchProtocol.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol\isearchprotocol.htm
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: ISearchProtocol, ISearchProtocol interface [search], ISearchProtocol interface [search],described, _search_ISearchProtocol, search._search_ISearchProtocol, searchapi/ISearchProtocol
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchProtocol
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchProtocol interface


## -description


Provides methods for invoking, initializing, and managing <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> objects. Methods in this interface are called by the protocol host when processing URLs from the gatherer. 
        


        The protocol handler implements the protocol for accessing a content source in its native format. Use this interface to implement a custom protocol handler to expand the data sources that can be indexed. 
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchProtocol</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchProtocol</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2334914c-baab-4c4b-963b-b3c48d9a96c6">CloseAccessor</a>
</td>
<td align="left" width="63%">

        Closes a previously created <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fa8bf02-155d-48e9-8f94-c54680ae33e2">CreateAccessor</a>
</td>
<td align="left" width="63%">

          Creates and initializes an <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object.  
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">

          Initializes a protocol handler. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">ShutDown</a>
</td>
<td align="left" width="63%">

            Shuts down the protocol handler.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/cfba12eb-4123-4b57-8311-d4fc8f9f514e">The Indexing Process</a>
 

 

