---
UID: NF:structuredquery.IEntity.Base
title: IEntity::Base (structuredquery.h)
description: Retrieves the parent entity of this entity.
helpviewer_keywords: ["Base","Base method [search]","Base method [search]","IEntity interface","IEntity interface [search]","Base method","IEntity.Base","IEntity::Base","_search_IEntity_Base","search._search_IEntity_Base","structuredquery/IEntity::Base"]
old-location: search\_search_IEntity_Base.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\base.htm
ms.date: 12/05/2018
ms.keywords: Base, Base method [search], Base method [search],IEntity interface, IEntity interface [search],Base method, IEntity.Base, IEntity::Base, _search_IEntity_Base, search._search_IEntity_Base, structuredquery/IEntity::Base
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
 - IEntity::Base
 - structuredquery/IEntity::Base
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
 - IEntity.Base
---

# IEntity::Base


## -description

Retrieves the parent entity of this entity.

## -parameters

### -param pBaseEntity [out, retval]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a>**</b>

Receives a pointer to the parent <a href="/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a> object, or <b>NULL</b> if there is no parent entity.

## -returns

Type: <b>HRESULT</b>

Returns one of the following, or an error value otherwise.
        

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
<i>pBaseEntity</i> successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The entity has no parent; <i>pBaseEntity</i> successfully set to <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Each entity derives from some other entity, except the entity named Entity, for which this method returns S_FALSE. The derived entity inherits all relationships from the base entity.