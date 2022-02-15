---
UID: NE:fwpmtypes.FWPM_PROVIDER_CONTEXT_TYPE_
title: FWPM_PROVIDER_CONTEXT_TYPE (fwpmtypes.h)
description: Types of provider contexts that may be stored in Base Filtering Engine (BFE).
helpviewer_keywords: ["FWPM_CLASSIFY_OPTIONS_CONTEXT","FWPM_GENERAL_CONTEXT","FWPM_IPSEC_AUTHIP_MM_CONTEXT","FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT","FWPM_IPSEC_AUTHIP_QM_TUNNEL_CONTEXT","FWPM_IPSEC_DOSP_CONTEXT","FWPM_IPSEC_IKEV2_MM_CONTEXT","FWPM_IPSEC_IKEV2_QM_TRANSPORT_CONTEXT","FWPM_IPSEC_IKEV2_QM_TUNNEL_CONTEXT","FWPM_IPSEC_IKE_MM_CONTEXT","FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT","FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT","FWPM_IPSEC_KEYING_CONTEXT","FWPM_PROVIDER_CONTEXT_TYPE","FWPM_PROVIDER_CONTEXT_TYPE enumeration [Filtering]","FWPM_PROVIDER_CONTEXT_TYPE_MAX","fwp.fwpm_provider_context_type_enum","fwpmtypes/FWPM_CLASSIFY_OPTIONS_CONTEXT","fwpmtypes/FWPM_GENERAL_CONTEXT","fwpmtypes/FWPM_IPSEC_AUTHIP_MM_CONTEXT","fwpmtypes/FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT","fwpmtypes/FWPM_IPSEC_AUTHIP_QM_TUNNEL_CONTEXT","fwpmtypes/FWPM_IPSEC_DOSP_CONTEXT","fwpmtypes/FWPM_IPSEC_IKEV2_MM_CONTEXT","fwpmtypes/FWPM_IPSEC_IKEV2_QM_TRANSPORT_CONTEXT","fwpmtypes/FWPM_IPSEC_IKEV2_QM_TUNNEL_CONTEXT","fwpmtypes/FWPM_IPSEC_IKE_MM_CONTEXT","fwpmtypes/FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT","fwpmtypes/FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT","fwpmtypes/FWPM_IPSEC_KEYING_CONTEXT","fwpmtypes/FWPM_PROVIDER_CONTEXT_TYPE","fwpmtypes/FWPM_PROVIDER_CONTEXT_TYPE_MAX"]
old-location: fwp\fwpm_provider_context_type_enum.htm
tech.root: fwp
ms.assetid: e8eae5e7-9240-47a5-851b-1ec51cb07b63
ms.date: 12/05/2018
ms.keywords: FWPM_CLASSIFY_OPTIONS_CONTEXT, FWPM_GENERAL_CONTEXT, FWPM_IPSEC_AUTHIP_MM_CONTEXT, FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT, FWPM_IPSEC_AUTHIP_QM_TUNNEL_CONTEXT, FWPM_IPSEC_DOSP_CONTEXT, FWPM_IPSEC_IKEV2_MM_CONTEXT, FWPM_IPSEC_IKEV2_QM_TRANSPORT_CONTEXT, FWPM_IPSEC_IKEV2_QM_TUNNEL_CONTEXT, FWPM_IPSEC_IKE_MM_CONTEXT, FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT, FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT, FWPM_IPSEC_KEYING_CONTEXT, FWPM_PROVIDER_CONTEXT_TYPE, FWPM_PROVIDER_CONTEXT_TYPE enumeration [Filtering], FWPM_PROVIDER_CONTEXT_TYPE_MAX, fwp.fwpm_provider_context_type_enum, fwpmtypes/FWPM_CLASSIFY_OPTIONS_CONTEXT, fwpmtypes/FWPM_GENERAL_CONTEXT, fwpmtypes/FWPM_IPSEC_AUTHIP_MM_CONTEXT, fwpmtypes/FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT, fwpmtypes/FWPM_IPSEC_AUTHIP_QM_TUNNEL_CONTEXT, fwpmtypes/FWPM_IPSEC_DOSP_CONTEXT, fwpmtypes/FWPM_IPSEC_IKEV2_MM_CONTEXT, fwpmtypes/FWPM_IPSEC_IKEV2_QM_TRANSPORT_CONTEXT, fwpmtypes/FWPM_IPSEC_IKEV2_QM_TUNNEL_CONTEXT, fwpmtypes/FWPM_IPSEC_IKE_MM_CONTEXT, fwpmtypes/FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT, fwpmtypes/FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT, fwpmtypes/FWPM_IPSEC_KEYING_CONTEXT, fwpmtypes/FWPM_PROVIDER_CONTEXT_TYPE, fwpmtypes/FWPM_PROVIDER_CONTEXT_TYPE_MAX
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
req.typenames: FWPM_PROVIDER_CONTEXT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_PROVIDER_CONTEXT_TYPE_
 - fwpmtypes/FWPM_PROVIDER_CONTEXT_TYPE_
 - FWPM_PROVIDER_CONTEXT_TYPE
 - fwpmtypes/FWPM_PROVIDER_CONTEXT_TYPE
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
 - FWPM_PROVIDER_CONTEXT_TYPE
---

# FWPM_PROVIDER_CONTEXT_TYPE enumeration


## -description

The <b>FWPM_PROVIDER_CONTEXT_TYPE</b> enumerated type specifies types of provider contexts that may be stored in Base Filtering Engine (BFE).

## -enum-fields

### -field FWPM_IPSEC_KEYING_CONTEXT:0

Specifies keying context type.

### -field FWPM_IPSEC_IKE_QM_TRANSPORT_CONTEXT

Specifies IPsec IKE quick mode transport context type.

### -field FWPM_IPSEC_IKE_QM_TUNNEL_CONTEXT

Specifies IPsec IKE quick mode tunnel context type.

### -field FWPM_IPSEC_AUTHIP_QM_TRANSPORT_CONTEXT

Specifies IPsec AuthIP quick mode transport context type.

### -field FWPM_IPSEC_AUTHIP_QM_TUNNEL_CONTEXT

Specifies IPsec Authip quick mode tunnel context type.

### -field FWPM_IPSEC_IKE_MM_CONTEXT

Specifies IKE main mode context type.

### -field FWPM_IPSEC_AUTHIP_MM_CONTEXT

Specifies AuthIP main mode context type.

### -field FWPM_CLASSIFY_OPTIONS_CONTEXT

Specifies classify options context type.

### -field FWPM_GENERAL_CONTEXT

Specifies general context type.

### -field FWPM_IPSEC_IKEV2_QM_TUNNEL_CONTEXT

Specifies IKE v2 quick mode tunnel context type.

<div class="alert"><b>Note</b>  Available only in Windows Server 2008 R2, Windows 7, and later.</div>
<div> </div>

### -field FWPM_IPSEC_IKEV2_MM_CONTEXT

Specifies IKE v2 main mode tunnel context type.

<div class="alert"><b>Note</b>  Available only in Windows Server 2008 R2, Windows 7, and later.</div>
<div> </div>

### -field FWPM_IPSEC_DOSP_CONTEXT

Specifies IPsec DoS Protection context type.

<div class="alert"><b>Note</b>  Available only in Windows Server 2008 R2, Windows 7, and later.</div>
<div> </div>

### -field FWPM_IPSEC_IKEV2_QM_TRANSPORT_CONTEXT

Specifies IKE v2 quick mode transport context type.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows 8.</div>
<div> </div>

### -field FWPM_PROVIDER_CONTEXT_TYPE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
