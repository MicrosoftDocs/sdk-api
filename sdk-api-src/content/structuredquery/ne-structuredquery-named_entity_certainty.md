---
UID: NE:structuredquery.__MIDL___MIDL_itf_structuredquery_0000_0012_0001
title: NAMED_ENTITY_CERTAINTY (structuredquery.h)
description: Defines the level of certainty for a named entity.
helpviewer_keywords: ["NAMED_ENTITY_CERTAINTY","NAMED_ENTITY_CERTAINTY enumeration [search]","NEC_HIGH","NEC_LOW","NEC_MEDIUM","_search_NAMED_ENTITY_CERTAINTY","search._search_NAMED_ENTITY_CERTAINTY","structuredquery/NAMED_ENTITY_CERTAINTY","structuredquery/NEC_HIGH","structuredquery/NEC_LOW","structuredquery/NEC_MEDIUM"]
old-location: search\_search_NAMED_ENTITY_CERTAINTY.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\named_entity_certainty.htm
ms.date: 12/05/2018
ms.keywords: NAMED_ENTITY_CERTAINTY, NAMED_ENTITY_CERTAINTY enumeration [search], NEC_HIGH, NEC_LOW, NEC_MEDIUM, _search_NAMED_ENTITY_CERTAINTY, search._search_NAMED_ENTITY_CERTAINTY, structuredquery/NAMED_ENTITY_CERTAINTY, structuredquery/NEC_HIGH, structuredquery/NEC_LOW, structuredquery/NEC_MEDIUM
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: NAMED_ENTITY_CERTAINTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_structuredquery_0000_0012_0001
 - structuredquery/__MIDL___MIDL_itf_structuredquery_0000_0012_0001
 - NAMED_ENTITY_CERTAINTY
 - structuredquery/NAMED_ENTITY_CERTAINTY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Structuredquery.h
api_name:
 - NAMED_ENTITY_CERTAINTY
---

# NAMED_ENTITY_CERTAINTY enumeration


## -description

Defines the level of certainty for a named entity.

## -enum-fields

### -field NEC_LOW:0

It could be this named entity but additional evidence is advisable.

### -field NEC_MEDIUM

It quite likely is this named entity; it is okay to use it.

### -field NEC_HIGH

It almost certainly is this named entity; it should be okay to discard other possibilities.

