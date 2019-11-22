---
UID: NF:structuredquery.IEntity.GetRelationship
title: IEntity::GetRelationship (structuredquery.h)

description: Retrieves the IRelationship object for this entity as requested by name.
old-location: search\_search_IEntity_GetRelationship.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\getrelationship.htm

ms.date: 12/05/2018
ms.keywords: GetRelationship, GetRelationship method [search], GetRelationship method [search],IEntity interface, IEntity interface [search],GetRelationship method, IEntity.GetRelationship, IEntity::GetRelationship, _search_IEntity_GetRelationship, search._search_IEntity_GetRelationship, structuredquery/IEntity::GetRelationship
ms.topic: method
f1_keywords: 
 - "structuredquery/IEntity.GetRelationship"
dev_langs:
 - c++
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
 - IEntity.GetRelationship
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IEntity::GetRelationship


## -description


Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-irelationship">IRelationship</a> object for this entity as requested by name.
        


## -parameters




### -param pszRelationName [in]

Type: <b>LPCWSTR</b>

The name of the relationship to find.
            


### -param pRelationship [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-irelationship">IRelationship</a>**</b>

Receives the address of a pointer to the requested <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-irelationship">IRelationship</a> object, or <b>NULL</b> if this entity has no relationship with the name specified.
            


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there is no matching relationship, or an error value otherwise.



