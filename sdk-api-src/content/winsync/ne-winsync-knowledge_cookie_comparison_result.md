---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0011
title: KNOWLEDGE_COOKIE_COMPARISON_RESULT (winsync.h)
description: Represents the possible results when a knowledge cookie is compared with a knowledge object by using ISyncKnowledge2::CompareToKnowledgeCookie.
helpviewer_keywords: ["KCCR_COOKIE_KNOWLEDGE_CONTAINED","KCCR_COOKIE_KNOWLEDGE_CONTAINS","KCCR_COOKIE_KNOWLEDGE_EQUAL","KCCR_COOKIE_KNOWLEDGE_NOT_COMPARABLE","KNOWLEDGE_COOKIE_COMPARISON_RESULT","KNOWLEDGE_COOKIE_COMPARISON_RESULT enumeration [Windows Sync]","winsync.knowledge_cookie_comparison_result","winsync/KCCR_COOKIE_KNOWLEDGE_CONTAINED","winsync/KCCR_COOKIE_KNOWLEDGE_CONTAINS","winsync/KCCR_COOKIE_KNOWLEDGE_EQUAL","winsync/KCCR_COOKIE_KNOWLEDGE_NOT_COMPARABLE","winsync/KNOWLEDGE_COOKIE_COMPARISON_RESULT"]
old-location: winsync\knowledge_cookie_comparison_result.htm
tech.root: winsync
ms.assetid: 9770679e-19ed-49ed-a505-076db6f0119c
ms.date: 12/05/2018
ms.keywords: KCCR_COOKIE_KNOWLEDGE_CONTAINED, KCCR_COOKIE_KNOWLEDGE_CONTAINS, KCCR_COOKIE_KNOWLEDGE_EQUAL, KCCR_COOKIE_KNOWLEDGE_NOT_COMPARABLE, KNOWLEDGE_COOKIE_COMPARISON_RESULT, KNOWLEDGE_COOKIE_COMPARISON_RESULT enumeration [Windows Sync], winsync.knowledge_cookie_comparison_result, winsync/KCCR_COOKIE_KNOWLEDGE_CONTAINED, winsync/KCCR_COOKIE_KNOWLEDGE_CONTAINS, winsync/KCCR_COOKIE_KNOWLEDGE_EQUAL, winsync/KCCR_COOKIE_KNOWLEDGE_NOT_COMPARABLE, winsync/KNOWLEDGE_COOKIE_COMPARISON_RESULT
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsync_0000_0000_0011
 - winsync/__MIDL___MIDL_itf_winsync_0000_0000_0011
 - KNOWLEDGE_COOKIE_COMPARISON_RESULT
 - winsync/KNOWLEDGE_COOKIE_COMPARISON_RESULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsync.h
api_name:
 - KNOWLEDGE_COOKIE_COMPARISON_RESULT
---

# KNOWLEDGE_COOKIE_COMPARISON_RESULT enumeration


## -description

Represents the possible results when a knowledge cookie is compared with a knowledge object by using <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-comparetoknowledgecookie">ISyncKnowledge2::CompareToKnowledgeCookie</a>.

## -enum-fields

### -field KCCR_COOKIE_KNOWLEDGE_EQUAL:0

The knowledge cookie is equal to the specified knowledge.

### -field KCCR_COOKIE_KNOWLEDGE_CONTAINED

The knowledge cookie is contained by the specified knowledge.

### -field KCCR_COOKIE_KNOWLEDGE_CONTAINS

The knowledge cookie contains the specified knowledge.

### -field KCCR_COOKIE_KNOWLEDGE_NOT_COMPARABLE

The knowledge cookie cannot be compared to the specified knowledge.

## -remarks

A knowledge cookie is a lightweight, read-only representation of knowledge that can be used for fast comparisons when performance is especially important.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-enumerations">Windows Sync Enumerations</a>
