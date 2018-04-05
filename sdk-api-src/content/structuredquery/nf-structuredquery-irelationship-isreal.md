---
UID: NF:structuredquery.IRelationship.IsReal
title: IRelationship::IsReal method
author: windows-driver-content
description: Reports whether a relationship is real.
old-location: search\_search_IRelationship_IsReal.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irelationship\isreal.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IRelationship, IRelationship interface [search], IsReal method, IRelationship::IsReal, IsReal method [search], IsReal method [search], IRelationship interface, IsReal,IRelationship.IsReal, _search_IRelationship_IsReal, search._search_IRelationship_IsReal, structuredquery/IRelationship::IsReal
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
-	IRelationship.IsReal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRelationship::IsReal method


## -description


Reports whether a relationship is real.


## -parameters




### -param pIsReal [out, retval]

Type: <b>BOOL*</b>

Receives <b>TRUE</b> for a real relationship; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        A relationship is not considered real if its source entity derives from an entity
        that has a relationship of the same name. The purpose of such a "shadow" relationship
        is to store metadata specific to the inherited relationship.
      



