---
UID: NC:fwpmu.FWPM_NET_EVENT_CALLBACK2
title: FWPM_NET_EVENT_CALLBACK2 (fwpmu.h)
description: Is used to add custom behavior to the net event subscription process. (FWPM_NET_EVENT_CALLBACK2)
helpviewer_keywords: ["FWPM_NET_EVENT_CALLBACK2","FWPM_NET_EVENT_CALLBACK2 callback","FWPM_NET_EVENT_CALLBACK2 callback function [Filtering]","fwp.fwpm_net_event_callback2","fwpmu/FWPM_NET_EVENT_CALLBACK2"]
old-location: fwp\fwpm_net_event_callback2.htm
tech.root: fwp
ms.assetid: 0A5E0ADB-0879-4646-9F69-D8AB9BD067AD
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_CALLBACK2, FWPM_NET_EVENT_CALLBACK2 callback, FWPM_NET_EVENT_CALLBACK2 callback function [Filtering], fwp.fwpm_net_event_callback2, fwpmu/FWPM_NET_EVENT_CALLBACK2
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - FWPM_NET_EVENT_CALLBACK2
 - fwpmu/FWPM_NET_EVENT_CALLBACK2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - fwpmu.h
api_name:
 - FWPM_NET_EVENT_CALLBACK2
---

# FWPM_NET_EVENT_CALLBACK2 callback function


## -description

The <b>FWPM_NET_EVENT_CALLBACK2</b> function is used to add custom behavior to the net event subscription process.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_CALLBACK2</b> is the specific implementation of FWPM_NET_EVENT_CALLBACK used in Windows 10, version 1607 and later. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1">FWPM_NET_EVENT_CALLBACK1</a> is available. For Windows 7, <a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback0">FWPM_NET_EVENT_CALLBACK0</a> is available.</div><div> </div>

## -parameters

### -param context [in, out]

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe2">FwpmNetEventSubscribe2</a> function.

### -param event [in]

An [FWPM_NET_EVENT3](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event3) struct that contains the event information.

## -remarks

Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe2">FwpmNetEventSubscribe2</a> to register this callback function.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe2">FwpmNetEventSubscribe2</a>
