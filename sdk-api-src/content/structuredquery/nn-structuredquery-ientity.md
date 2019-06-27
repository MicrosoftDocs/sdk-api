---
UID: NN:structuredquery.IEntity
title: IEntity (structuredquery.h)
author: windows-sdk-content
description: Provides methods for retrieving information about an entity type in the schema.
old-location: search\_search_IEntity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\ientity.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEntity, IEntity interface [search], IEntity interface [search],described, _search_IEntity, search._search_IEntity, structuredquery/IEntity
ms.topic: interface
f1_keywords: 
 - "structuredquery/IEntity"
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
 - IEntity
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IEntity interface


## -description


Provides methods for retrieving information about an entity type in the schema.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEntity</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEntity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEntity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-ientity-base">Base</a>
</td>
<td align="left" width="63%">
Retrieves the parent entity of this entity.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-ientity-defaultphrase">DefaultPhrase</a>
</td>
<td align="left" width="63%">
Retrieves a default phrase to use for this entity in restatements.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-ientity-getnamedentity">GetNamedEntity</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-inamedentity">INamedEntity</a> object based on an entity name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-ientity-getrelationship">GetRelationship</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-irelationship">IRelationship</a> object for this entity as requested by name.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-ientity-metadata">MetaData</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-imetadata">IMetaData</a> objects for this entity.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-ientity-name">Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of this entity.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-ientity-namedentities">NamedEntities</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-inamedentity">INamedEntity</a> objects, one for each known named entity of this type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-ientity-relationships">Relationships</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-irelationship">IRelationship</a> objects, one for each relationship this entity has.
        

</td>
</tr>
</table> 

