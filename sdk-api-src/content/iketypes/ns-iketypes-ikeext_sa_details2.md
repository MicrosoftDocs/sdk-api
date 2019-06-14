---
UID: NS:iketypes.IKEEXT_SA_DETAILS2_
title: IKEEXT_SA_DETAILS2 (iketypes.h)
author: windows-sdk-content
description: Is used to store information returned when enumerating IKE, AuthIP, and IKEv2 security associations (SAs).
old-location: fwp\ikeext_sa_details2.htm
tech.root: fwp
ms.assetid: 51b8f3a8-bccc-4d1f-871f-9a319ed5c49c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IKEEXT_SA_DETAILS2, IKEEXT_SA_DETAILS2 structure [Filtering], fwp.ikeext_sa_details2, iketypes/IKEEXT_SA_DETAILS2
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iketypes.h
api_name:
 - IKEEXT_SA_DETAILS2
product: Windows
targetos: Windows
req.typenames: IKEEXT_SA_DETAILS2
req.redist: 
ms.custom: 19H1
---

# IKEEXT_SA_DETAILS2 structure


## -description


The <b>IKEEXT_SA_DETAILS2</b> structure is used to store information returned when enumerating IKE, AuthIP, and IKEv2 security associations (SAs).
<div class="alert"><b>Note</b>  <b>IKEEXT_SA_DETAILS2</b> is the specific implementation of IKEEXT_SA_DETAILS used in Windows 8. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_sa_details1_">IKEEXT_SA_DETAILS1</a> is available. For Windows Vista, <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_sa_details0_">IKEEXT_SA_DETAILS0</a>  is available.</div><div> </div>

## -struct-fields




### -field saId

Type: <b>UINT64</b>

LUID identifying the security association.


### -field keyModuleType

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_key_module_type_">IKEEXT_KEY_MODULE_TYPE</a></b>

Key module type. 


### -field ipVersion

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version_">FWP_IP_VERSION</a></b>

 The IP version.


### -field v4UdpEncapsulation

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0_">IPSEC_V4_UDP_ENCAPSULATION0</a>*</b>

Stores the UDP ports corresponding to the 
   Main Mode, if a NAT is detected.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>. 


### -field ikeTraffic

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_traffic0_">IKEEXT_TRAFFIC0</a></b>

The traffic corresponding to this IKE SA.


### -field ikeProposal

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_proposal0_">IKEEXT_PROPOSAL0</a></b>

The main mode proposal corresponding to this IKE SA.


### -field cookiePair

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_cookie_pair0_">IKEEXT_COOKIE_PAIR0</a></b>

The SA cookies.


### -field ikeCredentials

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials2_">IKEEXT_CREDENTIALS2</a></b>

Credentials information for the SA.


### -field ikePolicyKey

Type: <b>GUID</b>

GUID of the main mode policy provider context corresponding to this SA.


### -field virtualIfTunnelId

Type: <b>UINT64</b>

ID/Handle to virtual interface tunneling state. Applicable only to IKEv2.


### -field correlationKey

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob_">FWP_BYTE_BLOB</a></b>

Key derived from authentications to allow external applications to cryptographically bind
   their exchanges with this SA.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob_">FWP_BYTE_BLOB</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version_">FWP_IP_VERSION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_cookie_pair0_">IKEEXT_COOKIE_PAIR0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials2_">IKEEXT_CREDENTIALS2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_key_module_type_">IKEEXT_KEY_MODULE_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_proposal0_">IKEEXT_PROPOSAL0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_traffic0_">IKEEXT_TRAFFIC0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0_">IPSEC_V4_UDP_ENCAPSULATION0</a>
 

 

