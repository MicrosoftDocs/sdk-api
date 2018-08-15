---
UID: NN:structuredquery.ISchemaProvider
title: ISchemaProvider
author: windows-sdk-content
description: Provides a schema repository that can be browsed.
old-location: search\_search_ISchemaProvider.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\ischemaprovider.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISchemaProvider, ISchemaProvider interface [search], ISchemaProvider interface [search],described, _search_ISchemaProvider, search._search_ISchemaProvider, structuredquery/ISchemaProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: structuredquery.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
 - ISchemaProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISchemaProvider interface


## -description


Provides a schema repository that can be browsed.
    	


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISchemaProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISchemaProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISchemaProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2c235a1-197c-4d09-8a88-b3e72ab8c4ff">Entities</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a> objects with one entry for each entity in the loaded schema.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/361be729-c65e-4012-bbfe-cdf3841eaa23">GetEntity</a>
</td>
<td align="left" width="63%">
Retrieves an entity by name from the loaded schema. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53bb8661-50c2-4932-a9b9-5a1a930a2302">Localize</a>
</td>
<td align="left" width="63%">
Localizes the currently loaded schema for a specified locale.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08a78c29-8cac-49de-be2d-8baffc8decf0">LookupAuthoredNamedEntity</a>
</td>
<td align="left" width="63%">
Finds named entities of a specified type in a tokenized string, and returns the value of the entity and the number of tokens the entity value occupies. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b52790b6-ef8e-411a-9a58-251ab648756c">MetaData</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of global <a href="https://msdn.microsoft.com/2647af6d-af05-4f0d-8613-03248385abec">IMetaData</a> objects for the loaded schema.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92e161ee-9b22-4ba6-a144-dc94abec80e8">RootEntity</a>
</td>
<td align="left" width="63%">
Retrieves the root entity of the loaded schema.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f65a8cf8-91f4-400e-9deb-303f103de48b">SaveBinary</a>
</td>
<td align="left" width="63%">
Saves the loaded schema as a schema binary at a specified path.

</td>
</tr>
</table> 

