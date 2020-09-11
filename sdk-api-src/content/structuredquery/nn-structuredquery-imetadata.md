---
UID: NN:structuredquery.IMetaData
title: IMetaData (structuredquery.h)
description: Provides a method for retrieving a key/value pair of strings from an IEntity, IRelationship or ISchemaProvider object.
helpviewer_keywords: ["IMetaData","IMetaData interface [search]","IMetaData interface [search]","described","_search_IMetaData","search._search_IMetaData","structuredquery/IMetaData"]
old-location: search\_search_IMetaData.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\imetadata\imetadata.htm
ms.date: 12/05/2018
ms.keywords: IMetaData, IMetaData interface [search], IMetaData interface [search],described, _search_IMetaData, search._search_IMetaData, structuredquery/IMetaData
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IMetaData
 - structuredquery/IMetaData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IMetaData
---

# IMetaData interface


## -description

Provides a method for retrieving a key/value pair of strings from an <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a>, <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-irelationship">IRelationship</a> or <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-ischemaprovider">ISchemaProvider</a> object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMetaData</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-imetadata-getdata">GetData</a>
</td>
<td align="left" width="63%">
Retrieves one key/value pair from the metadata of an <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a>, <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-irelationship">IRelationship</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-ischemaprovider">ISchemaProvider</a> object.

        

</td>
</tr>
</table>

