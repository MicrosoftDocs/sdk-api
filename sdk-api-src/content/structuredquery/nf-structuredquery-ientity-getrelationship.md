---
UID: NF:structuredquery.IEntity.GetRelationship
title: IEntity::GetRelationship method
author: windows-driver-content
description: Retrieves the IRelationship object for this entity as requested by name.
old-location: search\_search_IEntity_GetRelationship.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\getrelationship.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetRelationship method [search], GetRelationship method [search], IEntity interface, GetRelationship,IEntity.GetRelationship, IEntity, IEntity interface [search], GetRelationship method, IEntity::GetRelationship, _search_IEntity_GetRelationship, search._search_IEntity_GetRelationship, structuredquery/IEntity::GetRelationship
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Structuredquery.h
api_name:
-	IEntity.GetRelationship
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEntity::GetRelationship method


## -description



          Retrieves the <a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a> object for this entity as requested by name.
        


## -parameters




### -param pszRelationName [in]

Type: <b>LPCWSTR</b>


                The name of the relationship to find.
            


### -param pRelationship [out, retval]

Type: <b><a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a>**</b>


                Receives the address of a pointer to the requested <a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a> object, or <b>NULL</b> if this entity has no relationship with the name specified.
            


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there is no matching relationship, or an error value otherwise.



