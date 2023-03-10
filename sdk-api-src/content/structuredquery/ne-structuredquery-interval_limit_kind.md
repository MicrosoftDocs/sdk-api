---
UID: NE:structuredquery.tagINTERVAL_LIMIT_KIND
title: INTERVAL_LIMIT_KIND (structuredquery.h)
description: These values are returned by IInterval::GetLimits as pairs to specify a range with an upper and lower limit.
helpviewer_keywords: ["ILK_EXPLICIT_EXCLUDED","ILK_EXPLICIT_INCLUDED","ILK_NEGATIVE_INFINITY","ILK_POSITIVE_INFINITY","INTERVAL_LIMIT_KIND","INTERVAL_LIMIT_KIND enumeration [search]","_search_INTERVAL_LIMIT_KIND","search._search_INTERVAL_LIMIT_KIND","structuredquery/ILK_EXPLICIT_EXCLUDED","structuredquery/ILK_EXPLICIT_INCLUDED","structuredquery/ILK_NEGATIVE_INFINITY","structuredquery/ILK_POSITIVE_INFINITY","structuredquery/INTERVAL_LIMIT_KIND"]
old-location: search\_search_INTERVAL_LIMIT_KIND.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\interval_limit_kind.htm
ms.date: 12/05/2018
ms.keywords: ILK_EXPLICIT_EXCLUDED, ILK_EXPLICIT_INCLUDED, ILK_NEGATIVE_INFINITY, ILK_POSITIVE_INFINITY, INTERVAL_LIMIT_KIND, INTERVAL_LIMIT_KIND enumeration [search], _search_INTERVAL_LIMIT_KIND, search._search_INTERVAL_LIMIT_KIND, structuredquery/ILK_EXPLICIT_EXCLUDED, structuredquery/ILK_EXPLICIT_INCLUDED, structuredquery/ILK_NEGATIVE_INFINITY, structuredquery/ILK_POSITIVE_INFINITY, structuredquery/INTERVAL_LIMIT_KIND
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: INTERVAL_LIMIT_KIND
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - tagINTERVAL_LIMIT_KIND
 - structuredquery/tagINTERVAL_LIMIT_KIND
 - INTERVAL_LIMIT_KIND
 - structuredquery/INTERVAL_LIMIT_KIND
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
 - INTERVAL_LIMIT_KIND
---

# INTERVAL_LIMIT_KIND enumeration


## -description

These values are returned by <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iinterval-getlimits">IInterval::GetLimits</a> as pairs to specify a range with an upper and lower limit. <b>INTERVAL_LIMIT_KIND</b> identifies whether the ranges include or exclude the upper and lower values of the range, and whether a range begins or ends in infinity.

## -enum-fields

### -field ILK_EXPLICIT_INCLUDED:0

The value is included in the range. For example, an integer range of numbers that is equal to or greater than 3 and less than or equal to 6 includes both 3 and 6. So the values 3 and 6 would both be returned with <b>ILK_EXPLICIT_INCLUDED</b>.

### -field ILK_EXPLICIT_EXCLUDED

The value bounds the range but is not included in the range. For example, an integer range that is greater than 3 but less than 6 excludes both 3 and 6. So the values would both be returned with <b>ILK_EXPLICIT_EXCLUDED</b>.

### -field ILK_NEGATIVE_INFINITY

This is typically used as a lower bound. The specified value is ignored because the range begins (or ends) at negative infinity. For example, an integer range that includes every value less than 6 would have <b>ILK_NEGATIVE_INFINITY</b> for the lower bound and 6 and <b>ILK_EXPLICIT_EXCLUDED</b> for the upper bound.

### -field ILK_POSITIVE_INFINITY

This is typically used as an upper bound. The specified value is ignored because the range begins (or ends) at positive infinity. For example, an integer range that includes every value greater than or equal to 3 would have <b>ILK_EXPLICIT_INCLUDED</b> and 3 for the lower bound and <b>ILK_POSITIVE_INFINITY</b> for the upper bound.
