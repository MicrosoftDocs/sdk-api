---
UID: NN:structuredquery.ITokenCollection
title: ITokenCollection
author: windows-sdk-content
description: Gets the tokens that result from using a word breaker.
old-location: search\_search_ITokenCollection.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\itokencollection\itokencollection.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITokenCollection, ITokenCollection interface [search], ITokenCollection interface [search],described, _search_ITokenCollection, search._search_ITokenCollection, structuredquery/ITokenCollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
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
 - Structuredquery.h
api_name:
 - ITokenCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ITokenCollection interface


## -description


Gets the tokens that result from using a word breaker.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITokenCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITokenCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITokenCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29f34228-4e9c-4d43-9888-37f04505d312">GetToken</a>
</td>
<td align="left" width="63%">
Retrieves the position, length, and any overriding string of an individual token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f58d43e2-5488-4d2a-907b-62799a2f0615">NumberOfTokens</a>
</td>
<td align="left" width="63%">
Retrieves the number of tokens in the collection.

</td>
</tr>
</table> 

