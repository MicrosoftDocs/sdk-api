---
UID: NS:drt._DRT_ADDRESS_LIST
title: DRT_ADDRESS_LIST (drt.h)
description: DRT_ADDRESS_LIST structure contains a set of DRT_ADDRESS structures that represent the nodes contacted during a search for a key.
helpviewer_keywords: ["*PDRT_ADDRESS_LIST","DRT_ADDRESS_LIST","DRT_ADDRESS_LIST structure [Peer Networking]","PDRT_ADDRESS_LIST","PDRT_ADDRESS_LIST structure pointer [Peer Networking]","drt/DRT_ADDRESS_LIST","drt/PDRT_ADDRESS_LIST","p2p.drt_address_list"]
old-location: p2p\drt_address_list.htm
tech.root: p2p
ms.assetid: a795dff7-4182-42ad-b14b-142a6c1312c7
ms.date: 12/05/2018
ms.keywords: '*PDRT_ADDRESS_LIST, DRT_ADDRESS_LIST, DRT_ADDRESS_LIST structure [Peer Networking], PDRT_ADDRESS_LIST, PDRT_ADDRESS_LIST structure pointer [Peer Networking], drt/DRT_ADDRESS_LIST, drt/PDRT_ADDRESS_LIST, p2p.drt_address_list'
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
req.typenames: DRT_ADDRESS_LIST, *PDRT_ADDRESS_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DRT_ADDRESS_LIST
 - drt/_DRT_ADDRESS_LIST
 - PDRT_ADDRESS_LIST
 - drt/PDRT_ADDRESS_LIST
 - DRT_ADDRESS_LIST
 - drt/DRT_ADDRESS_LIST
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
 - DRT_ADDRESS_LIST
---

# DRT_ADDRESS_LIST structure


## -description

The <b>DRT_ADDRESS_LIST</b> structure contains a set of  <a href="/windows/desktop/api/drt/ns-drt-drt_address">DRT_ADDRESS</a> structures that represent the nodes contacted during a search for a key.

## -struct-fields

### -field AddressCount

The count of entries in <b>AddressList</b>.

### -field AddressList

An array of <a href="/windows/desktop/api/drt/ns-drt-drt_address">DRT_ADDRESS</a> structures that contain information about addresses that participated  in the search operation.

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_address">DRT_ADDRESS</a>



<a href="/windows/desktop/api/drt/nf-drt-drtgetsearchresult">DrtGetSearchResult</a>