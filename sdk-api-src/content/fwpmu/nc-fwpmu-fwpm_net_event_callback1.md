---
UID: NC:fwpmu.FWPM_NET_EVENT_CALLBACK1
title: FWPM_NET_EVENT_CALLBACK1 (fwpmu.h)
description: Is used to add custom behavior to the net event subscription process. (FWPM_NET_EVENT_CALLBACK1)
helpviewer_keywords: ["FWPM_NET_EVENT_CALLBACK1","FWPM_NET_EVENT_CALLBACK1 callback","FWPM_NET_EVENT_CALLBACK1 callback function [Filtering]","fwp.fwpm_net_event_callback1","fwpmu/FWPM_NET_EVENT_CALLBACK1"]
old-location: fwp\fwpm_net_event_callback1.htm
tech.root: fwp
ms.assetid: fddf8e2e-e133-4575-a6dc-c7b5e6cfff31
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_CALLBACK1, FWPM_NET_EVENT_CALLBACK1 callback, FWPM_NET_EVENT_CALLBACK1 callback function [Filtering], fwp.fwpm_net_event_callback1, fwpmu/FWPM_NET_EVENT_CALLBACK1
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
 - FWPM_NET_EVENT_CALLBACK1
 - fwpmu/FWPM_NET_EVENT_CALLBACK1
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
 - FWPM_NET_EVENT_CALLBACK1
---

# FWPM_NET_EVENT_CALLBACK1 callback function


## -description

The <b>FWPM_NET_EVENT_CALLBACK1</b> function is used to add custom behavior to the net event subscription process.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_CALLBACK1</b> is the specific implementation of FWPM_NET_EVENT_CALLBACK used in Windows 8 and later. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="/windows/win32/api/fwpmu/nc-fwpmu-fwpm_net_event_callback0">FWPM_NET_EVENT_CALLBACK0</a> is available.</div><div> </div>

## -parameters

### -param context [in, out]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="/windows/win32/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1">FwpmNetEventSubscribe1</a> function.

### -param event [in]

Type: <b>const <a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event2">FWPM_NET_EVENT2</a>*</b>

The net event information.

## -remarks

Call <a href="/windows/win32/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1">FwpmNetEventSubscribe1</a> to register this callback function.
