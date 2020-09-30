---
UID: NS:fwpmtypes.FWPM_VSWITCH_EVENT_SUBSCRIPTION0_
title: FWPM_VSWITCH_EVENT_SUBSCRIPTION0 (fwpmtypes.h)
description: Stores information used to subscribe to notifications about a vSwitch event.
helpviewer_keywords: ["FWPM_VSWITCH_EVENT_SUBSCRIPTION0","FWPM_VSWITCH_EVENT_SUBSCRIPTION0 structure [Filtering]","fwp.fwpm_vswitch_event_subscription0","fwpmtypes/FWPM_VSWITCH_EVENT_SUBSCRIPTION0"]
old-location: fwp\fwpm_vswitch_event_subscription0.htm
tech.root: fwp
ms.assetid: f099d531-ab40-4661-b33f-a805a84fba7e
ms.date: 12/05/2018
ms.keywords: FWPM_VSWITCH_EVENT_SUBSCRIPTION0, FWPM_VSWITCH_EVENT_SUBSCRIPTION0 structure [Filtering], fwp.fwpm_vswitch_event_subscription0, fwpmtypes/FWPM_VSWITCH_EVENT_SUBSCRIPTION0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_VSWITCH_EVENT_SUBSCRIPTION0_
 - fwpmtypes/FWPM_VSWITCH_EVENT_SUBSCRIPTION0_
 - FWPM_VSWITCH_EVENT_SUBSCRIPTION0
 - fwpmtypes/FWPM_VSWITCH_EVENT_SUBSCRIPTION0
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
 - FWPM_VSWITCH_EVENT_SUBSCRIPTION0
---

# FWPM_VSWITCH_EVENT_SUBSCRIPTION0 structure


## -description

The <b>FWPM_VSWITCH_EVENT_SUBSCRIPTION0</b> structure stores information used to subscribe to notifications about a vSwitch event.

## -struct-fields

### -field flags

Type: <b>UINT32</b>

This member is reserved for future use.

### -field sessionKey

Type: <b>GUID</b>

Identifies the session which created the subscription.

## -remarks

<b>FWPM_VSWITCH_EVENT_SUBSCRIPTION0</b> is a specific implementation of FWPM_VSWITCH_EVENT_SUBSCRIPTION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0">FwpmvSwitchEventSubscribe0</a>