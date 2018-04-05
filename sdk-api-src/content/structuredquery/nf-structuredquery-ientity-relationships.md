---
UID: NF:structuredquery.IEntity.Relationships
title: IEntity::Relationships method
author: windows-driver-content
description: Retrieves an enumeration of IRelationship objects, one for each relationship this entity has.
old-location: search\_search_IEntity_Relationships.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\relationships.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IEntity, IEntity interface [search], Relationships method, IEntity::Relationships, Relationships method [search], Relationships method [search], IEntity interface, Relationships,IEntity.Relationships, _search_IEntity_Relationships, search._search_IEntity_Relationships, structuredquery/IEntity::Relationships
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
-	IEntity.Relationships
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEntity::Relationships method


## -description



          Retrieves an enumeration of <a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a> objects, one for each relationship this entity has.
        


## -parameters




### -param riid [in]

Type: <b>REFIID</b>


                The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.
            


### -param pRelationships [out, retval]

Type: <b>void**</b>


                Receives the address of a pointer to the enumeration of the <a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a> objects.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



