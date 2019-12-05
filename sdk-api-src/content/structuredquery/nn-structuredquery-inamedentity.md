---
UID: NN:structuredquery.INamedEntity
title: INamedEntity (structuredquery.h)
description: Provides methods to get the value of, or a default phrase for the value of, a named entity.
old-location: search\_search_INamedEntity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\inamedentity\inamedentity.htm
ms.date: 12/05/2018
ms.keywords: INamedEntity, INamedEntity interface [search], INamedEntity interface [search],described, _search_INamedEntity, search._search_INamedEntity, structuredquery/INamedEntity
ms.topic: interface
f1_keywords:
- structuredquery/INamedEntity
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
- INamedEntity
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# INamedEntity interface


## -description


Provides methods to get the value of, or a default phrase for the value of, a named entity.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INamedEntity</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INamedEntity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INamedEntity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-inamedentity-defaultphrase">DefaultPhrase</a>
</td>
<td align="left" width="63%">
Retrieves a default phrase to use for this named entity in restatements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-inamedentity-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of this named entity as a string.

</td>
</tr>
</table> 

