---
UID: NS:drt.drt_search_info_tag
title: DRT_SEARCH_INFO (drt.h)
description: DRT_SEARCH_INFO structure represents a search query issued with DrtStartSearch.
helpviewer_keywords: ["*PDRT_SEARCH_INFO","DRT_SEARCH_INFO","DRT_SEARCH_INFO structure [Peer Networking]","PDRT_SEARCH_INFO","PDRT_SEARCH_INFO structure pointer [Peer Networking]","drt/DRT_SEARCH_INFO","drt/PDRT_SEARCH_INFO","p2p.drt_search_info"]
old-location: p2p\drt_search_info.htm
tech.root: p2p
ms.assetid: a3f12d8a-95ef-4168-8d2d-c317ae2c57b4
ms.date: 12/05/2018
ms.keywords: '*PDRT_SEARCH_INFO, DRT_SEARCH_INFO, DRT_SEARCH_INFO structure [Peer Networking], PDRT_SEARCH_INFO, PDRT_SEARCH_INFO structure pointer [Peer Networking], drt/DRT_SEARCH_INFO, drt/PDRT_SEARCH_INFO, p2p.drt_search_info'
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
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
req.typenames: DRT_SEARCH_INFO, *PDRT_SEARCH_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - drt_search_info_tag
 - drt/drt_search_info_tag
 - PDRT_SEARCH_INFO
 - drt/PDRT_SEARCH_INFO
 - DRT_SEARCH_INFO
 - drt/DRT_SEARCH_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_SEARCH_INFO
---

# DRT_SEARCH_INFO structure


## -description

The <b>DRT_SEARCH_INFO</b> structure represents a search query issued with <a href="/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a>.

## -struct-fields

### -field dwSize

Specifies the byte count of <b>DRT_SEARCH_INFO</b>.

### -field fIterative

Indicates whether the search is iterative.  If set to <b>TRUE</b>, the search is iterative.

### -field fAllowCurrentInstanceMatch

Indicates whether  search results can contain matches found in the local DRT instance.  If set to <b>TRUE</b>,  the search results are capable of containing matches found in the local DRT instance.

### -field fAnyMatchInRange

If set to <b>true</b>,   the search will stop locating the first key falling within the specified range. Otherwise, the search for the closest match to the target key specified by <a href="/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a> will continue.

### -field cMaxEndpoints

Specifies the number of results to return.  This includes closest and exact matches.   If this value is greater than 1 when <b>fIterative</b> is <b>TRUE</b>, the search will only return 1 result.

### -field pMaximumKey

Specifies the numerically largest key value the infrastructure should attempt to match.

### -field pMinimumKey

Specifies the numerically smallest key value the infrastructure should attempt to match.

## -see-also

<a href="/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a>