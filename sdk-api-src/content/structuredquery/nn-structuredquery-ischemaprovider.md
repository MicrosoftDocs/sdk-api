---
UID: NN:structuredquery.ISchemaProvider
title: ISchemaProvider (structuredquery.h)
author: windows-sdk-content
description: Provides a schema repository that can be browsed.
old-location: search\_search_ISchemaProvider.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\ischemaprovider.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISchemaProvider, ISchemaProvider interface [search], ISchemaProvider interface [search],described, _search_ISchemaProvider, search._search_ISchemaProvider, structuredquery/ISchemaProvider
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
 - ISchemaProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/en-us/library/Bb231324(v=VS.85).aspx">Entities</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://msdn.microsoft.com/en-us/library/Bb231373(v=VS.85).aspx">IEntity</a> objects with one entry for each entity in the loaded schema.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231325(v=VS.85).aspx">GetEntity</a>
</td>
<td align="left" width="63%">
Retrieves an entity by name from the loaded schema. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231327(v=VS.85).aspx">Localize</a>
</td>
<td align="left" width="63%">
Localizes the currently loaded schema for a specified locale.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231328(v=VS.85).aspx">LookupAuthoredNamedEntity</a>
</td>
<td align="left" width="63%">
Finds named entities of a specified type in a tokenized string, and returns the value of the entity and the number of tokens the entity value occupies. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231329(v=VS.85).aspx">MetaData</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of global <a href="https://msdn.microsoft.com/en-us/library/Bb231366(v=VS.85).aspx">IMetaData</a> objects for the loaded schema.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231330(v=VS.85).aspx">RootEntity</a>
</td>
<td align="left" width="63%">
Retrieves the root entity of the loaded schema.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231331(v=VS.85).aspx">SaveBinary</a>
</td>
<td align="left" width="63%">
Saves the loaded schema as a schema binary at a specified path.

</td>
</tr>
</table> 

