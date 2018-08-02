---
UID: NN:structuredquery.IEntity
title: IEntity
author: windows-sdk-content
description: Provides methods for retrieving information about an entity type in the schema.
old-location: search\_search_IEntity.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\ientity.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IEntity, IEntity interface [search], IEntity interface [search],described, _search_IEntity, search._search_IEntity, structuredquery/IEntity
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
tech.root: 
req.typenames: NAMED_ENTITY_CERTAINTY
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEntity interface


## -description


Provides methods for retrieving information about an entity type in the schema.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEntity</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEntity</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Bb231369(v=VS.85).aspx">Base</a>
</td>
<td align="left" width="63%">
Retrieves the parent entity of this entity.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231370(v=VS.85).aspx">DefaultPhrase</a>
</td>
<td align="left" width="63%">
Retrieves a default phrase to use for this entity in restatements.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231371(v=VS.85).aspx">GetNamedEntity</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Bb231364(v=VS.85).aspx">INamedEntity</a> object based on an entity name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231372(v=VS.85).aspx">GetRelationship</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/en-us/library/Bb231339(v=VS.85).aspx">IRelationship</a> object for this entity as requested by name.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn915567">MetaData</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://msdn.microsoft.com/en-us/library/Bb231366(v=VS.85).aspx">IMetaData</a> objects for this entity.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of this entity.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231376(v=VS.85).aspx">NamedEntities</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://msdn.microsoft.com/en-us/library/Bb231364(v=VS.85).aspx">INamedEntity</a> objects, one for each known named entity of this type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231377(v=VS.85).aspx">Relationships</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://msdn.microsoft.com/en-us/library/Bb231339(v=VS.85).aspx">IRelationship</a> objects, one for each relationship this entity has.
        

</td>
</tr>
</table> 

