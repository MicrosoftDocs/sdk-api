---
UID: NS:fwpmtypes.FWPM_NET_EVENT0_
title: FWPM_NET_EVENT0 (fwpmtypes.h)
description: Contains information about all event types.
helpviewer_keywords: ["FWPM_NET_EVENT0","FWPM_NET_EVENT0 structure [Filtering]","fwp.fwpm_net_event0","fwpmtypes/FWPM_NET_EVENT0"]
old-location: fwp\fwpm_net_event0.htm
tech.root: fwp
ms.assetid: 91e15135-49b8-497e-8f09-984e9af64dbe
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT0, FWPM_NET_EVENT0 structure [Filtering], fwp.fwpm_net_event0, fwpmtypes/FWPM_NET_EVENT0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FWPM_NET_EVENT0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT0_
 - fwpmtypes/FWPM_NET_EVENT0_
 - FWPM_NET_EVENT0
 - fwpmtypes/FWPM_NET_EVENT0
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
 - FWPM_NET_EVENT0
---

# FWPM_NET_EVENT0 structure


## -description

The <b>FWPM_NET_EVENT0</b> structure contains information about all event types.
[FWPM_NET_EVENT1](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event1) is available. For Windows 8, [FWPM_NET_EVENT2](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event2) is available.</div><div> </div>

## -struct-fields

### -field header

A [FWPM_NET_EVENT_HEADER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header0) structure that contains information common to all events.

### -field type

A [FWPM_NET_EVENT_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) value that specifies the type of event.

### -field ikeMmFailure

Address of an <a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure0">FWPM_NET_EVENT_IKEEXT_MM_FAILURE0</a> structure that contains information about  an IKE main mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE</b>.

### -field ikeQmFailure

Address of an <a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0">FWPM_NET_EVENT_IKEEXT_QM_FAILURE0</a> structure that contains information about  an IKE quick mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE</b>.

### -field ikeEmFailure

Address of an <a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure0">FWPM_NET_EVENT_IKEEXT_EM_FAILURE0</a> structure that contains information about  an IKE user mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE</b>.

### -field classifyDrop

Address of an [FWPM_NET_EVENT_CLASSIFY_DROP0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0) structure that contains information about  a drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_CLASSIFY_DROP</b>.

### -field ipsecDrop

Address of an <a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0">FWPM_NET_EVENT_IPSEC_KERNEL_DROP0</a> structure that contains information about an IPsec kernel drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP</b>.

### -field idpDrop

Address of an <a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0">FWPM_NET_EVENT_IPSEC_DOSP_DROP0</a> structure that contains information about an IPsec DoS Protection event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_IPSEC_DOSP_DROP</b>.

<div class="alert"><b>Note</b>  Available only in Windows Server 2008 R2, Windows 7, and later.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>