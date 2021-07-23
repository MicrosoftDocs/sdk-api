---
UID: NF:structuredquery.IRelationship.IsReal
title: IRelationship::IsReal (structuredquery.h)
description: Reports whether a relationship is real.
helpviewer_keywords: ["IRelationship interface [search]","IsReal method","IRelationship.IsReal","IRelationship::IsReal","IsReal","IsReal method [search]","IsReal method [search]","IRelationship interface","_search_IRelationship_IsReal","search._search_IRelationship_IsReal","structuredquery/IRelationship::IsReal"]
old-location: search\_search_IRelationship_IsReal.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irelationship\isreal.htm
ms.date: 12/05/2018
ms.keywords: IRelationship interface [search],IsReal method, IRelationship.IsReal, IRelationship::IsReal, IsReal, IsReal method [search], IsReal method [search],IRelationship interface, _search_IRelationship_IsReal, search._search_IRelationship_IsReal, structuredquery/IRelationship::IsReal
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
 - IRelationship::IsReal
 - structuredquery/IRelationship::IsReal
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
 - IRelationship.IsReal
---

# IRelationship::IsReal


## -description

Reports whether a relationship is real.

## -parameters

### -param pIsReal [out, retval]

Type: <b>BOOL*</b>

Receives <b>TRUE</b> for a real relationship; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A relationship is not considered real if its source entity derives from an entity
        that has a relationship of the same name. The purpose of such a "shadow" relationship
        is to store metadata specific to the inherited relationship.

