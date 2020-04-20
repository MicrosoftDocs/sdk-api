---
UID: NS:drt.drt_search_result_tag
title: DRT_SEARCH_RESULT (drt.h)
description: DRT_SEARCH_RESULT.helpviewer_keywords: ["*PDRT_SEARCH_RESULT","DRT_SEARCH_RESULT","DRT_SEARCH_RESULT structure [Peer Networking]","PDRT_SEARCH_RESULT","PDRT_SEARCH_RESULT structure pointer [Peer Networking]","drt/DRT_SEARCH_RESULT","drt/PDRT_SEARCH_RESULT","p2p.drt_search_result"]
old-location: p2p\drt_search_result.htm
tech.root: P2PSdk
ms.assetid: 23cf713e-2730-456c-a3da-649c5ed00ffb
ms.date: 12/05/2018
ms.keywords: '*PDRT_SEARCH_RESULT, DRT_SEARCH_RESULT, DRT_SEARCH_RESULT structure [Peer Networking], PDRT_SEARCH_RESULT, PDRT_SEARCH_RESULT structure pointer [Peer Networking], drt/DRT_SEARCH_RESULT, drt/PDRT_SEARCH_RESULT, p2p.drt_search_result'
f1_keywords:
- drt/DRT_SEARCH_RESULT
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- drt.h
api_name:
- DRT_SEARCH_RESULT
targetos: Windows
req.typenames: DRT_SEARCH_RESULT, *PDRT_SEARCH_RESULT
req.redist: 
ms.custom: 19H1
---

# DRT_SEARCH_RESULT structure


## -description


The <b>DRT_SEARCH_RESULT</b> contains the registration entry and the type of match of the search result returned by <a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtgetsearchresult">DrtGetSearchResult</a> when the <i>hEvent</i> passed into  <a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a> is signaled.


## -struct-fields




### -field dwSize

The size of the <b>DRT_SEARCH_RESULT</b> structure.


### -field type

Specifies  the exactness of the search. This member corresponds to the <a href="https://docs.microsoft.com/windows/desktop/api/drt/ne-drt-drt_match_type">DRT_MATCH_TYPE</a> enumeration.


### -field pvContext

Pointer to the context data passed to the <a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a> API.


### -field registration

Contains the registration result.


#### - addressList

The address that the DRT protocol is bound to on the node that corresponds to the search result. This structure can be used to debug connectivity issues between nodes.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/drt/ne-drt-drt_match_type">DRT_MATCH_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtgetsearchresult">DrtGetSearchResult</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a>
 

 

