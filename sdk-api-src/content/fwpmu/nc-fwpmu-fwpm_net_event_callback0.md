---
UID: NC:fwpmu.FWPM_NET_EVENT_CALLBACK0
title: FWPM_NET_EVENT_CALLBACK0 (fwpmu.h)
description: Is used to add custom behavior to the net event subscription process. (FWPM_NET_EVENT_CALLBACK0)
helpviewer_keywords: ["FWPM_NET_EVENT_CALLBACK0","FWPM_NET_EVENT_CALLBACK0 callback","FWPM_NET_EVENT_CALLBACK0 callback function [Filtering]","fwp.fwpm_net_event_callback0_func","fwpmu/FWPM_NET_EVENT_CALLBACK0"]
old-location: fwp\fwpm_net_event_callback0_func.htm
tech.root: fwp
ms.assetid: 69b311c5-ac08-490b-823b-4049f7c46975
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_CALLBACK0, FWPM_NET_EVENT_CALLBACK0 callback, FWPM_NET_EVENT_CALLBACK0 callback function [Filtering], fwp.fwpm_net_event_callback0_func, fwpmu/FWPM_NET_EVENT_CALLBACK0
req.header: fwpmu.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_CALLBACK0
 - fwpmu/FWPM_NET_EVENT_CALLBACK0
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
 - FWPM_NET_EVENT_CALLBACK0
---

# FWPM_NET_EVENT_CALLBACK0 callback function


## -description

The <b>FWPM_NET_EVENT_CALLBACK0</b> function is used to add custom behavior to the net event subscription process.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_CALLBACK0</b> is the specific implementation of FWPM_NET_EVENT_CALLBACK used in Windows 7. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1">FWPM_NET_EVENT_CALLBACK1</a> is available.</div><div> </div>

## -parameters

### -param context [in, out]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe0">FwpmNetEventSubscribe0</a> function.

### -param event [in]

Type: [FWPM_NET_EVENT1](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event1)*</b>

The net event information.

## -remarks

Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe0">FwpmNetEventSubscribe0</a> to register this callback function.

## -see-also

[FWPM_NET_EVENT1](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event1)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe0">FwpmNetEventSubscribe0</a>
