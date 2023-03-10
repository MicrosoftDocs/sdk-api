---
UID: NS:fwpmtypes.FWPM_NET_EVENT_SUBSCRIPTION0_
title: FWPM_NET_EVENT_SUBSCRIPTION0 (fwpmtypes.h)
description: Stores information used to subscribe to notifications about a network event.
helpviewer_keywords: ["FWPM_NET_EVENT_SUBSCRIPTION0","FWPM_NET_EVENT_SUBSCRIPTION0 structure [Filtering]","fwp.fwpm_net_event_subscription0","fwpmtypes/FWPM_NET_EVENT_SUBSCRIPTION0"]
old-location: fwp\fwpm_net_event_subscription0.htm
tech.root: fwp
ms.assetid: a1aa8369-fd70-46f6-983d-0afdf8b8ff77
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_SUBSCRIPTION0, FWPM_NET_EVENT_SUBSCRIPTION0 structure [Filtering], fwp.fwpm_net_event_subscription0, fwpmtypes/FWPM_NET_EVENT_SUBSCRIPTION0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_NET_EVENT_SUBSCRIPTION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_SUBSCRIPTION0_
 - fwpmtypes/FWPM_NET_EVENT_SUBSCRIPTION0_
 - FWPM_NET_EVENT_SUBSCRIPTION0
 - fwpmtypes/FWPM_NET_EVENT_SUBSCRIPTION0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_SUBSCRIPTION0
---

# FWPM_NET_EVENT_SUBSCRIPTION0 structure


## -description

The <b>FWPM_NET_EVENT_SUBSCRIPTION0</b> structure stores information used to subscribe to notifications about a network event.

## -struct-fields

### -field enumTemplate

Address of an [FWPM_NET_EVENT_ENUM_TEMPLATE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_enum_template0) structure. Notifications are only dispatched for objects that match the template. If
   <b>enumTemplate</b> is <b>NULL</b>, it matches all objects.

### -field flags

Unused.

### -field sessionKey

Identifies the session which created the subscription.

## -remarks

<b>FWPM_NET_EVENT_SUBSCRIPTION0</b> is a specific implementation of FWPM_NET_EVENT_SUBSCRIPTION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.