---
UID: NE:structuredquery.CASE_REQUIREMENT
title: CASE_REQUIREMENT (structuredquery.h)
description: Specifies the case requirements of keywords, if any, for a query.
helpviewer_keywords: ["CASE_REQUIREMENT","CASE_REQUIREMENT enumeration [search]","CASE_REQUIREMENT_ANY","CASE_REQUIREMENT_UPPER_IF_AQS","_search_CASE_REQUIREMENT","search._search_CASE_REQUIREMENT","structuredquery/CASE_REQUIREMENT","structuredquery/CASE_REQUIREMENT_ANY","structuredquery/CASE_REQUIREMENT_UPPER_IF_AQS"]
old-location: search\_search_CASE_REQUIREMENT.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\case_requirement.htm
ms.date: 12/05/2018
ms.keywords: CASE_REQUIREMENT, CASE_REQUIREMENT enumeration [search], CASE_REQUIREMENT_ANY, CASE_REQUIREMENT_UPPER_IF_AQS, _search_CASE_REQUIREMENT, search._search_CASE_REQUIREMENT, structuredquery/CASE_REQUIREMENT, structuredquery/CASE_REQUIREMENT_ANY, structuredquery/CASE_REQUIREMENT_UPPER_IF_AQS
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: CASE_REQUIREMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CASE_REQUIREMENT
 - structuredquery/CASE_REQUIREMENT
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
 - CASE_REQUIREMENT
---

# CASE_REQUIREMENT enumeration


## -description

Specifies the case requirements of keywords, if any, for a query.

## -enum-fields

### -field CASE_REQUIREMENT_ANY:0

Keywords are recognized regardless of case.

### -field CASE_REQUIREMENT_UPPER_IF_AQS

Keywords are recognized only if uppercase when AQS is the syntax. When AQS is not the syntax, keywords are recognized regardless of case.

## -remarks

Keywords include Boolean operators such as AND, NOT, and OR.

## -see-also

<a href="/windows/desktop/api/structuredquery/ne-structuredquery-structured_query_resolve_option">STRUCTURED_QUERY_RESOLVE_OPTION</a>
