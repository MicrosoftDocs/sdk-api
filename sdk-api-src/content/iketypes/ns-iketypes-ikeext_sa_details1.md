---
UID: NS:iketypes.IKEEXT_SA_DETAILS1_
title: IKEEXT_SA_DETAILS1 (iketypes.h)
description: Is used to store information returned when enumerating IKE, AuthIP, and IKEv2 security associations (SAs). (IKEEXT_SA_DETAILS1)
helpviewer_keywords: ["IKEEXT_SA_DETAILS1","IKEEXT_SA_DETAILS1 structure [Filtering]","fwp.ikeext_sa_details1","iketypes/IKEEXT_SA_DETAILS1"]
old-location: fwp\ikeext_sa_details1.htm
tech.root: fwp
ms.assetid: b4b8767b-399a-49f0-91fd-59c2206742de
ms.date: 12/05/2018
ms.keywords: IKEEXT_SA_DETAILS1, IKEEXT_SA_DETAILS1 structure [Filtering], fwp.ikeext_sa_details1, iketypes/IKEEXT_SA_DETAILS1
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_SA_DETAILS1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_SA_DETAILS1_
 - iketypes/IKEEXT_SA_DETAILS1_
 - IKEEXT_SA_DETAILS1
 - iketypes/IKEEXT_SA_DETAILS1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_SA_DETAILS1
---

# IKEEXT_SA_DETAILS1 structure


## -description

The <b>IKEEXT_SA_DETAILS1</b> structure is used to store information returned when enumerating IKE, AuthIP, and IKEv2 security associations (SAs).
[IKEEXT_SA_DETAILS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_sa_details0) is available.</div><div> </div>

## -struct-fields

### -field saId

LUID identifying the security association.

### -field keyModuleType

Key module type. 

See [IKEEXT_KEY_MODULE_TYPE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_key_module_type) for more information.

### -field ipVersion

IP version specified by [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version).

### -field v4UdpEncapsulation

Points to an  [IPSEC_V4_UDP_ENCAPSULATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0) structure, which, if a NAT is detected,  stores the UDP ports corresponding to the 
   Main Mode.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field ikeTraffic

The traffic corresponding to this IKE SA specified by [IKEEXT_TRAFFIC0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_traffic0).

### -field ikeProposal

The main mode proposal corresponding to this IKE SA specified by [IKEEXT_PROPOSAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_proposal0).

### -field cookiePair

SA cookies specified by [IKEEXT_COOKIE_PAIR0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cookie_pair0).

### -field ikeCredentials

Credentials information for the SA specified by [IKEEXT_CREDENTIALS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials1).

### -field ikePolicyKey

GUID of the main mode policy provider context corresponding to this SA.

### -field virtualIfTunnelId

ID/Handle to virtual interface tunneling state. Applicable only to IKEv2.

### -field correlationKey

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
