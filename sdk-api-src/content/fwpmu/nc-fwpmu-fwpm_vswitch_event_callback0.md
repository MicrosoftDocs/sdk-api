---
UID: NC:fwpmu.FWPM_VSWITCH_EVENT_CALLBACK0
title: FWPM_VSWITCH_EVENT_CALLBACK0 (fwpmu.h)
description: Is used to add custom behavior to the vSwitch event subscription process.
helpviewer_keywords: ["FWPM_VSWITCH_EVENT_CALLBACK0","FWPM_VSWITCH_EVENT_CALLBACK0 callback","FWPM_VSWITCH_EVENT_CALLBACK0 callback function [Filtering]","fwp.fwpm_vswitch_event_callback0","fwpmu/FWPM_VSWITCH_EVENT_CALLBACK0"]
old-location: fwp\fwpm_vswitch_event_callback0.htm
tech.root: fwp
ms.assetid: 95cccc54-8f58-4942-8770-f07f4d293396
ms.date: 12/05/2018
ms.keywords: FWPM_VSWITCH_EVENT_CALLBACK0, FWPM_VSWITCH_EVENT_CALLBACK0 callback, FWPM_VSWITCH_EVENT_CALLBACK0 callback function [Filtering], fwp.fwpm_vswitch_event_callback0, fwpmu/FWPM_VSWITCH_EVENT_CALLBACK0
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_VSWITCH_EVENT_CALLBACK0
 - fwpmu/FWPM_VSWITCH_EVENT_CALLBACK0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Fwpmu.h
api_name:
 - FWPM_VSWITCH_EVENT_CALLBACK0
---

# FWPM_VSWITCH_EVENT_CALLBACK0 callback function


## -description

The <b>FWPM_VSWITCH_EVENT_CALLBACK0</b> function is used to add custom behavior to the vSwitch event subscription process.

## -parameters

### -param context [in, out]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0">FwpmvSwitchEventSubscribe0</a> function.

### -param vSwitchEvent [in]

Type: [FWPM_VSWITCH_EVENT0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)*</b>

The vSwitch event information.

## -returns

This callback function does not return a value.

## -remarks

Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0">FwpmvSwitchEventSubscribe0</a> to register this callback function.

<b>FWPM_VSWITCH_EVENT_CALLBACK0</b> is a specific implementation of FWPM_VSWITCH_EVENT_CALLBACK. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_VSWITCH_EVENT0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0">FwpmvSwitchEventSubscribe0</a>
