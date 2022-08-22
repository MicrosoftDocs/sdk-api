---
UID: NS:iketypes.IKEEXT_SA_DETAILS2_
title: IKEEXT_SA_DETAILS2 (iketypes.h)
description: Is used to store information returned when enumerating IKE, AuthIP, and IKEv2 security associations (SAs). (IKEEXT_SA_DETAILS2)
helpviewer_keywords: ["IKEEXT_SA_DETAILS2","IKEEXT_SA_DETAILS2 structure [Filtering]","fwp.ikeext_sa_details2","iketypes/IKEEXT_SA_DETAILS2"]
old-location: fwp\ikeext_sa_details2.htm
tech.root: fwp
ms.assetid: 51b8f3a8-bccc-4d1f-871f-9a319ed5c49c
ms.date: 12/05/2018
ms.keywords: IKEEXT_SA_DETAILS2, IKEEXT_SA_DETAILS2 structure [Filtering], fwp.ikeext_sa_details2, iketypes/IKEEXT_SA_DETAILS2
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: IKEEXT_SA_DETAILS2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_SA_DETAILS2_
 - iketypes/IKEEXT_SA_DETAILS2_
 - IKEEXT_SA_DETAILS2
 - iketypes/IKEEXT_SA_DETAILS2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iketypes.h
api_name:
 - IKEEXT_SA_DETAILS2
---

# IKEEXT_SA_DETAILS2 structure


## -description

The <b>IKEEXT_SA_DETAILS2</b> structure is used to store information returned when enumerating IKE, AuthIP, and IKEv2 security associations (SAs).
[IKEEXT_SA_DETAILS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_sa_details1) is available. For Windows Vista, [IKEEXT_SA_DETAILS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_sa_details0)  is available.</div><div> </div>

## -struct-fields

### -field saId

Type: <b>UINT64</b>

LUID identifying the security association.

### -field keyModuleType

Type: [IKEEXT_KEY_MODULE_TYPE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_key_module_type)</b>

Key module type.

### -field ipVersion

Type: [FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)</b>

 The IP version.

### -field v4UdpEncapsulation

Type: [IPSEC_V4_UDP_ENCAPSULATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)*</b>

Stores the UDP ports corresponding to the 
   Main Mode, if a NAT is detected.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.

### -field ikeTraffic

Type: [IKEEXT_TRAFFIC0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_traffic0)</b>

The traffic corresponding to this IKE SA.

### -field ikeProposal

Type: [IKEEXT_PROPOSAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_proposal0)</b>

The main mode proposal corresponding to this IKE SA.

### -field cookiePair

Type: [IKEEXT_COOKIE_PAIR0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cookie_pair0)</b>

The SA cookies.

### -field ikeCredentials

Type: [IKEEXT_CREDENTIALS2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials2)</b>

Credentials information for the SA.

### -field ikePolicyKey

Type: <b>GUID</b>

GUID of the main mode policy provider context corresponding to this SA.

### -field virtualIfTunnelId

Type: <b>UINT64</b>

ID/Handle to virtual interface tunneling state. Applicable only to IKEv2.

### -field correlationKey

Type: [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)</b>

Key derived from authentications to allow external applications to cryptographically bind
   their exchanges with this SA.

## -see-also

[FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)



[FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)



[IKEEXT_COOKIE_PAIR0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_cookie_pair0)



[IKEEXT_CREDENTIALS2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials2)



[IKEEXT_KEY_MODULE_TYPE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_key_module_type)



[IKEEXT_PROPOSAL0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_proposal0)



[IKEEXT_TRAFFIC0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_traffic0)



[IPSEC_V4_UDP_ENCAPSULATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
