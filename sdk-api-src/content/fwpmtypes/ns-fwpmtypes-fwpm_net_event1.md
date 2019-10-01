---
UID: NS:fwpmtypes.FWPM_NET_EVENT1_
title: FWPM_NET_EVENT1 (fwpmtypes.h)
author: windows-sdk-content
description: Contains information about all event types.
old-location: fwp\fwpm_net_event1.htm
tech.root: fwp
ms.assetid: 0f989f66-8373-4546-ade3-8b337c4507e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT1, FWPM_NET_EVENT1 structure [Filtering], fwp.fwpm_net_event1, fwpmtypes/FWPM_NET_EVENT1
ms.topic: struct
f1_keywords: 
 - "fwpmtypes/FWPM_NET_EVENT1"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_NET_EVENT1
targetos: Windows
req.typenames: FWPM_NET_EVENT1
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT1 structure


## -description


The <b>FWPM_NET_EVENT1</b> structure contains information about all event types.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT1</b> is the specific implementation of FWPM_NET_EVENT used in Windows 7. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event2_">FWPM_NET_EVENT2</a> is available. For Windows Vista, <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event0_">FWPM_NET_EVENT0</a> is available.</div><div> </div>

## -struct-fields




### -field header

An <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header1_">FWPM_NET_EVENT_HEADER1</a> structure that contains information common to all events.


### -field type

An <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_net_event_type_">FWPM_NET_EVENT_TYPE</a> value that specifies the type of event.


### -field ikeMmFailure

Address of an <a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1">FWPM_NET_EVENT_IKEEXT_MM_FAILURE1</a> structure that contains information about  an IKE main mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE</b>.


### -field ikeQmFailure

Address of an <a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0">FWPM_NET_EVENT_IKEEXT_QM_FAILURE0</a> structure that contains information about  an IKE quick mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE</b>.


### -field ikeEmFailure

Address of an <a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1">FWPM_NET_EVENT_IKEEXT_EM_FAILURE1</a> structure that contains information about  an IKE user mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE</b>.


### -field classifyDrop

Address of an <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop1_">FWPM_NET_EVENT_CLASSIFY_DROP1</a> structure that contains information about  a drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_CLASSIFY_DROP</b>.


### -field ipsecDrop

Address of an <a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0">FWPM_NET_EVENT_IPSEC_KERNEL_DROP0</a> structure that contains information about an IPsec kernel drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP</b>.


### -field idpDrop

Address of an <a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0">FWPM_NET_EVENT_IPSEC_DOSP_DROP0</a> structure that contains information about an IPsec DoS Protection event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_IPSEC_DOSP_DROP</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

