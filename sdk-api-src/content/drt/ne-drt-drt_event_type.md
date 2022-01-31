---
UID: NE:drt.drt_event_type_tag
title: DRT_EVENT_TYPE (drt.h)
description: The DRT_EVENT_TYPE enumeration defines the set of events that can be raised by the Distributed Routing Table.
helpviewer_keywords: ["DRT_EVENT_LEAFSET_KEY_CHANGED","DRT_EVENT_REGISTRATION_STATE_CHANGED","DRT_EVENT_STATUS_CHANGED","DRT_EVENT_TYPE","DRT_EVENT_TYPE enumeration [Peer Networking]","drt/DRT_EVENT_LEAFSET_KEY_CHANGED","drt/DRT_EVENT_REGISTRATION_STATE_CHANGED","drt/DRT_EVENT_STATUS_CHANGED","drt/DRT_EVENT_TYPE","p2p.drt_event_type"]
old-location: p2p\drt_event_type.htm
tech.root: p2p
ms.assetid: 8125e663-10dd-4c3d-b9d6-ac6164b9f0a4
ms.date: 12/05/2018
ms.keywords: DRT_EVENT_LEAFSET_KEY_CHANGED, DRT_EVENT_REGISTRATION_STATE_CHANGED, DRT_EVENT_STATUS_CHANGED, DRT_EVENT_TYPE, DRT_EVENT_TYPE enumeration [Peer Networking], drt/DRT_EVENT_LEAFSET_KEY_CHANGED, drt/DRT_EVENT_REGISTRATION_STATE_CHANGED, drt/DRT_EVENT_STATUS_CHANGED, drt/DRT_EVENT_TYPE, p2p.drt_event_type
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
req.typenames: DRT_EVENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - drt_event_type_tag
 - drt/drt_event_type_tag
 - DRT_EVENT_TYPE
 - drt/DRT_EVENT_TYPE
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
 - DRT_EVENT_TYPE
---

# DRT_EVENT_TYPE enumeration


## -description

The <b>DRT_EVENT_TYPE</b> enumeration defines the set of events that can be raised by the Distributed Routing Table.

## -enum-fields

### -field DRT_EVENT_STATUS_CHANGED:0

The status of the local DRT instance has changed.

### -field DRT_EVENT_LEAFSET_KEY_CHANGED:1

A key or node was changed from the DRT leaf set of the local node.

### -field DRT_EVENT_REGISTRATION_STATE_CHANGED:2

A locally published key is no longer resolvable by other nodes.

## -remarks

The event handle passed to <a href="/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a> is signaled with an event  specified by the <b>DRT_EVENT_TYPE</b> enumeration.

## -see-also

<a href="/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>
