---
UID: NE:drt.drt_match_type_tag
title: DRT_MATCH_TYPE (drt.h)
description: The DRT_MATCH_TYPE enumeration defines the exactness of a search result returned by DrtGetSearchResult after initiating a search with the DrtStartSearch API.
helpviewer_keywords: ["DRT_MATCH_EXACT","DRT_MATCH_INTERMEDIATE","DRT_MATCH_NEAR","DRT_MATCH_TYPE","DRT_MATCH_TYPE enumeration [Peer Networking]","drt/DRT_MATCH_EXACT","drt/DRT_MATCH_INTERMEDIATE","drt/DRT_MATCH_NEAR","drt/DRT_MATCH_TYPE","p2p.drt_match_type"]
old-location: p2p\drt_match_type.htm
tech.root: p2p
ms.assetid: ab6e3a91-bd40-4a5e-889e-4d9c7279a4a3
ms.date: 12/05/2018
ms.keywords: DRT_MATCH_EXACT, DRT_MATCH_INTERMEDIATE, DRT_MATCH_NEAR, DRT_MATCH_TYPE, DRT_MATCH_TYPE enumeration [Peer Networking], drt/DRT_MATCH_EXACT, drt/DRT_MATCH_INTERMEDIATE, drt/DRT_MATCH_NEAR, drt/DRT_MATCH_TYPE, p2p.drt_match_type
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
req.typenames: DRT_MATCH_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - drt_match_type_tag
 - drt/drt_match_type_tag
 - DRT_MATCH_TYPE
 - drt/DRT_MATCH_TYPE
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
 - DRT_MATCH_TYPE
---

# DRT_MATCH_TYPE enumeration


## -description

The <b>DRT_MATCH_TYPE</b> enumeration defines the exactness of a search result returned by <a href="/windows/desktop/api/drt/nf-drt-drtgetsearchresult">DrtGetSearchResult</a> after initiating  a search with the <a href="/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a> API.

## -enum-fields

### -field DRT_MATCH_EXACT:0

The node  found is publishing the target key or is publishing a key within the specified range.

### -field DRT_MATCH_NEAR:1

The node found is publishing the numerically closest key to the specified target key.

### -field DRT_MATCH_INTERMEDIATE:2

The node returned is  an intermediate node. An application will  receive this node match type if <b>fIterative</b> is set to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/drt/nf-drt-drtgetsearchresult">DrtGetSearchResult</a>



<a href="/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a>
