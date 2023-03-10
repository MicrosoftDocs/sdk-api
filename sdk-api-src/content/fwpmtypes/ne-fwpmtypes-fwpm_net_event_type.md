---
UID: NE:fwpmtypes.FWPM_NET_EVENT_TYPE_
title: FWPM_NET_EVENT_TYPE (fwpmtypes.h)
description: Type of net event.
helpviewer_keywords: ["FWPM_NET_EVENT_TYPE","FWPM_NET_EVENT_TYPE enumeration [Filtering]","FWPM_NET_EVENT_TYPE_CAPABILITY_ALLOW","FWPM_NET_EVENT_TYPE_CAPABILITY_DROP","FWPM_NET_EVENT_TYPE_CLASSIFY_ALLOW","FWPM_NET_EVENT_TYPE_CLASSIFY_DROP","FWPM_NET_EVENT_TYPE_CLASSIFY_DROP_MAC","FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE","FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE","FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE","FWPM_NET_EVENT_TYPE_IPSEC_DOSP_DROP","FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP","FWPM_NET_EVENT_TYPE_MAX","fwp.fwpm_net_event_type","fwpmtypes/FWPM_NET_EVENT_TYPE","fwpmtypes/FWPM_NET_EVENT_TYPE_CAPABILITY_ALLOW","fwpmtypes/FWPM_NET_EVENT_TYPE_CAPABILITY_DROP","fwpmtypes/FWPM_NET_EVENT_TYPE_CLASSIFY_ALLOW","fwpmtypes/FWPM_NET_EVENT_TYPE_CLASSIFY_DROP","fwpmtypes/FWPM_NET_EVENT_TYPE_CLASSIFY_DROP_MAC","fwpmtypes/FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE","fwpmtypes/FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE","fwpmtypes/FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE","fwpmtypes/FWPM_NET_EVENT_TYPE_IPSEC_DOSP_DROP","fwpmtypes/FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP","fwpmtypes/FWPM_NET_EVENT_TYPE_MAX"]
old-location: fwp\fwpm_net_event_type.htm
tech.root: fwp
ms.assetid: 75dd3b0f-d809-421e-ac70-b8bf5d38757c
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_TYPE, FWPM_NET_EVENT_TYPE enumeration [Filtering], FWPM_NET_EVENT_TYPE_CAPABILITY_ALLOW, FWPM_NET_EVENT_TYPE_CAPABILITY_DROP, FWPM_NET_EVENT_TYPE_CLASSIFY_ALLOW, FWPM_NET_EVENT_TYPE_CLASSIFY_DROP, FWPM_NET_EVENT_TYPE_CLASSIFY_DROP_MAC, FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE, FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE, FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE, FWPM_NET_EVENT_TYPE_IPSEC_DOSP_DROP, FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP, FWPM_NET_EVENT_TYPE_MAX, fwp.fwpm_net_event_type, fwpmtypes/FWPM_NET_EVENT_TYPE, fwpmtypes/FWPM_NET_EVENT_TYPE_CAPABILITY_ALLOW, fwpmtypes/FWPM_NET_EVENT_TYPE_CAPABILITY_DROP, fwpmtypes/FWPM_NET_EVENT_TYPE_CLASSIFY_ALLOW, fwpmtypes/FWPM_NET_EVENT_TYPE_CLASSIFY_DROP, fwpmtypes/FWPM_NET_EVENT_TYPE_CLASSIFY_DROP_MAC, fwpmtypes/FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE, fwpmtypes/FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE, fwpmtypes/FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE, fwpmtypes/FWPM_NET_EVENT_TYPE_IPSEC_DOSP_DROP, fwpmtypes/FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP, fwpmtypes/FWPM_NET_EVENT_TYPE_MAX
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
req.typenames: FWPM_NET_EVENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_TYPE_
 - fwpmtypes/FWPM_NET_EVENT_TYPE_
 - FWPM_NET_EVENT_TYPE
 - fwpmtypes/FWPM_NET_EVENT_TYPE
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
 - FWPM_NET_EVENT_TYPE
---

# FWPM_NET_EVENT_TYPE enumeration


## -description

The <b>FWPM_NET_EVENT_TYPE</b> enumerated type specifies the type of net event.

## -enum-fields

### -field FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE:0

An IKE/AuthIP main mode failure has occurred.

### -field FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE

An IKE/AuthIP quick mode failure has occurred.

### -field FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE

An AuthIP extended mode failure has occurred.

### -field FWPM_NET_EVENT_TYPE_CLASSIFY_DROP

A drop event has occurred.

### -field FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP

An IPsec kernel drop event has occurred.

### -field FWPM_NET_EVENT_TYPE_IPSEC_DOSP_DROP

An IPsec DoS Protection drop event has occurred.

<div class="alert"><b>Note</b>  Available only in Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>

### -field FWPM_NET_EVENT_TYPE_CLASSIFY_ALLOW

An allow event has occurred.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field FWPM_NET_EVENT_TYPE_CAPABILITY_DROP

An app container network capability drop event has occurred.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field FWPM_NET_EVENT_TYPE_CAPABILITY_ALLOW

An app container network capability allow event has occurred.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field FWPM_NET_EVENT_TYPE_CLASSIFY_DROP_MAC

A MAC layer drop event has occurred.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field FWPM_NET_EVENT_TYPE_LPM_PACKET_ARRIVAL

### -field FWPM_NET_EVENT_TYPE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
