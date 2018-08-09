---
UID: NF:structuredquery.IEntity.NamedEntities
title: IEntity::NamedEntities
author: windows-sdk-content
description: Retrieves an enumeration of INamedEntity objects, one for each known named entity of this type.
old-location: search\_search_IEntity_NamedEntities.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\namedentities.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IEntity interface [search],NamedEntities method, IEntity.NamedEntities, IEntity::NamedEntities, NamedEntities, NamedEntities method [search], NamedEntities method [search],IEntity interface, _search_IEntity_NamedEntities, search._search_IEntity_NamedEntities, structuredquery/IEntity::NamedEntities
ms.prod: windows
ms.technology: windows-sdk
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
 - IEntity.NamedEntities
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEntity::NamedEntities


## -description


Retrieves an enumeration of <a href="https://msdn.microsoft.com/1e5dfef8-0f54-4302-97d8-bcbc0edbef03">INamedEntity</a> objects, one for each known named entity of this type.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.


### -param pNamedEntities [out, retval]

Type: <b>void**</b>

Receives the address of a pointer to an enumeration of <a href="https://msdn.microsoft.com/1e5dfef8-0f54-4302-97d8-bcbc0edbef03">INamedEntity</a> objects, one for each known named entity of this type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



