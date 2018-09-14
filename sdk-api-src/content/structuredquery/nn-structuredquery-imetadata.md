---
UID: NN:structuredquery.IMetaData
title: IMetaData
author: windows-sdk-content
description: Provides a method for retrieving a key/value pair of strings from an IEntity, IRelationship or ISchemaProvider object.
old-location: search\_search_IMetaData.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\imetadata\imetadata.htm
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMetaData, IMetaData interface [search], IMetaData interface [search],described, _search_IMetaData, search._search_IMetaData, structuredquery/IMetaData
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
 - IMetaData
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IMetaData interface


## -description


Provides a method for retrieving a key/value pair of strings from an <a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a>, <a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a> or <a href="https://msdn.microsoft.com/c6cb1da0-5072-41b2-aa64-e39c8c97b2f8">ISchemaProvider</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaData</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMetaData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMetaData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c044dca9-0e74-454b-8c9a-3ef8267d316d">GetData</a>
</td>
<td align="left" width="63%">
Retrieves one key/value pair from the metadata of an <a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a>, <a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a>, or <a href="https://msdn.microsoft.com/c6cb1da0-5072-41b2-aa64-e39c8c97b2f8">ISchemaProvider</a> object.

        

</td>
</tr>
</table> 

