---
UID: NN:structuredquery.IEntity
title: IEntity
author: windows-sdk-content
description: Provides methods for retrieving information about an entity type in the schema.
old-location: search\_search_IEntity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\ientity.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IEntity, IEntity interface [search], IEntity interface [search],described, _search_IEntity, search._search_IEntity, structuredquery/IEntity
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
 - IEntity
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
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
<a href="https://msdn.microsoft.com/6b65dd1e-5d8e-4147-bcc2-abf99930be04">Base</a>
</td>
<td align="left" width="63%">
Retrieves the parent entity of this entity.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/429c59ce-237a-45af-8862-53f371955e0b">DefaultPhrase</a>
</td>
<td align="left" width="63%">
Retrieves a default phrase to use for this entity in restatements.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa1a5324-3c23-4e6c-9e97-1a08996a6093">GetNamedEntity</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/1e5dfef8-0f54-4302-97d8-bcbc0edbef03">INamedEntity</a> object based on an entity name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e6fbe71-d95f-49df-b41b-95102f1fb8aa">GetRelationship</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a> object for this entity as requested by name.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb375a52-ded1-432a-bfb9-451cd4161ff7">MetaData</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://msdn.microsoft.com/2647af6d-af05-4f0d-8613-03248385abec">IMetaData</a> objects for this entity.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfff36b8-0b3b-4673-b788-d612ff840989">Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of this entity.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fa7e1be-7e01-4bc6-a797-a040a456966d">NamedEntities</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://msdn.microsoft.com/1e5dfef8-0f54-4302-97d8-bcbc0edbef03">INamedEntity</a> objects, one for each known named entity of this type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8b33485-8ded-4db2-b691-ba73e6cf7801">Relationships</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a> objects, one for each relationship this entity has.
        

</td>
</tr>
</table> 

