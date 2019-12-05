---
UID: NN:structuredquery.ITokenCollection
title: ITokenCollection (structuredquery.h)
description: Gets the tokens that result from using a word breaker.
old-location: search\_search_ITokenCollection.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\itokencollection\itokencollection.htm
ms.date: 12/05/2018
ms.keywords: ITokenCollection, ITokenCollection interface [search], ITokenCollection interface [search],described, _search_ITokenCollection, search._search_ITokenCollection, structuredquery/ITokenCollection
ms.topic: interface
f1_keywords:
- structuredquery/ITokenCollection
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ITokenCollection interface


## -description


Gets the tokens that result from using a word breaker.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITokenCollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITokenCollection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-itokencollection-gettoken">GetToken</a>
</td>
<td align="left" width="63%">
Retrieves the position, length, and any overriding string of an individual token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-itokencollection-numberoftokens">NumberOfTokens</a>
</td>
<td align="left" width="63%">
Retrieves the number of tokens in the collection.

</td>
</tr>
</table> 

