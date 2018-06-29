---
UID: NN:searchapi.ISearchProtocolThreadContext
title: ISearchProtocolThreadContext
author: windows-sdk-content
description: This optional interface enables the protocol handler to perform an action on the thread used for filtering in the protocol host.
old-location: search\_search_ISearchProtocolThreadContext.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocolthreadcontext\isearchprotocolthreadcontext.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISearchProtocolThreadContext, ISearchProtocolThreadContext interface [search], ISearchProtocolThreadContext interface [search],described, _search_ISearchProtocolThreadContext, search._search_ISearchProtocolThreadContext, searchapi/ISearchProtocolThreadContext
ms.prod: windows
ms.technology: windows-sdk
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
req.idl: Urlacc.idl
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
 - ISearchProtocolThreadContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchProtocolThreadContext interface


## -description


This optional interface enables the protocol handler to perform an action on the thread used for filtering in the protocol host. When the protocol host starts, it first initializes all the protocol handlers, and then it creates the filtering thread(s). The methods on this interface enable protocol handlers to manage their resources that are used by a filtering thread.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchProtocolThreadContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchProtocolThreadContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchProtocolThreadContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb231428(v=VS.85).aspx">ThreadIdle</a>
</td>
<td align="left" width="63%">
Notifies the protocol handler that the filtering thread is idle, so that the protocol handler can clean up any cache it might have built up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb231429(v=VS.85).aspx">ThreadInit</a>
</td>
<td align="left" width="63%">
Initializes communication between the protocol handler and the protocol host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb231430(v=VS.85).aspx">ThreadShutdown</a>
</td>
<td align="left" width="63%">
Notifies the protocol handler that the thread is being shut down.

</td>
</tr>
</table> 

