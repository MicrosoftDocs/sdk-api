---
UID: NN:structuredquery.INamedEntity
title: INamedEntity
author: windows-sdk-content
description: Provides methods to get the value of, or a default phrase for the value of, a named entity.
old-location: search\_search_INamedEntity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\inamedentity\inamedentity.htm
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: INamedEntity, INamedEntity interface [search], INamedEntity interface [search],described, _search_INamedEntity, search._search_INamedEntity, structuredquery/INamedEntity
ms.prod: windows
ms.technology: windows-sdk
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
 - INamedEntity
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# INamedEntity interface


## -description


Provides methods to get the value of, or a default phrase for the value of, a named entity.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INamedEntity</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INamedEntity</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b502c6fd-6b17-4abf-9a88-0ba168ff41f3">DefaultPhrase</a>
</td>
<td align="left" width="63%">
Retrieves a default phrase to use for this named entity in restatements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d12bd497-2fb9-41be-933d-ab97f3420522">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of this named entity as a string.

</td>
</tr>
</table> 

