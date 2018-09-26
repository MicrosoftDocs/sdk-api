---
UID: NN:structuredquery.IRelationship
title: IRelationship
author: windows-sdk-content
description: Provides methods for retrieving information about a schema property.
old-location: search\_search_IRelationship.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irelationship\irelationship.htm
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IRelationship, IRelationship interface [search], IRelationship interface [search],described, _search_IRelationship, search._search_IRelationship, structuredquery/IRelationship
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
 - IRelationship
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IRelationship interface


## -description


Provides methods for retrieving information about a schema property.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRelationship</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRelationship</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRelationship</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a2cc04a-40ca-4555-b2ea-471e3db8e69a">DefaultPhrase</a>
</td>
<td align="left" width="63%">
Retrieves the default phrase to use for this relationship in restatements.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d538c98c-73bb-4173-b031-579f3e7270ac">Destination</a>
</td>
<td align="left" width="63%">
Retrieves the destination <a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a> object of the relationship. The destination of a relationshipo corresponds to the type of a property.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a209437-a382-4a28-9e1c-9eea51669791">IsReal</a>
</td>
<td align="left" width="63%">
Reports whether a relationship is real.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3322f0c-8929-4f0f-8d2d-44f063ff83db">MetaData</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of <a href="https://msdn.microsoft.com/2647af6d-af05-4f0d-8613-03248385abec">IMetaData</a> objects for this relationship.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d1078d9-9f61-48ab-8317-f1be12027393">Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of the relationship.
      

</td>
</tr>
</table> 

