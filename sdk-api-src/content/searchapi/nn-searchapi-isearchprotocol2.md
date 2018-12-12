---
UID: NN:searchapi.ISearchProtocol2
title: ISearchProtocol2
author: windows-sdk-content
description: Provides methods for invoking, initializing, and managing IUrlAccessor objects.
old-location: search\_search_ISearchProtocol2.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol2\isearchprotocol2.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISearchProtocol2, ISearchProtocol2 interface [search], ISearchProtocol2 interface [search],described, _search_ISearchProtocol2, search._search_ISearchProtocol2, searchapi/ISearchProtocol2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchProtocol2 interface


## -description


Provides methods for invoking, initializing, and managing <a href="https://msdn.microsoft.com/en-us/library/Bb231426(v=VS.85).aspx">IUrlAccessor</a> objects. Methods in this interface are called by the protocol host when processing URLs from the gatherer. 
      

 
      The protocol handler implements the protocol for accessing a content source in its native format. Use this interface to implement a custom protocol handler to expand the data sources that can be indexed. 
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchProtocol2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb231440(v=VS.85).aspx">ISearchProtocol</a>. <b>ISearchProtocol2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Bb231433(v=VS.85).aspx">CreateAccessorEx</a>
</td>
<td align="left" width="63%">
 
        Creates and initializes an <a href="https://msdn.microsoft.com/en-us/library/Bb231426(v=VS.85).aspx">IUrlAccessor</a> object. This method has the same basic functionality as the <a href="https://msdn.microsoft.com/en-us/library/Bb231438(v=VS.85).aspx">ISearchProtocol::CreateAccessor</a> method, but it includes an additional <b>pUserData</b> parameter to supply additional data to the protocol handler.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb231440(v=VS.85).aspx">ISearchProtocol</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc678933(v=VS.85).aspx">The Indexing Process</a>
 

 

