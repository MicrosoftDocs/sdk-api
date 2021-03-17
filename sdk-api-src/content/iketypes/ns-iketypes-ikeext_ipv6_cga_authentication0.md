---
UID: NS:iketypes.IKEEXT_IPV6_CGA_AUTHENTICATION0_
title: IKEEXT_IPV6_CGA_AUTHENTICATION0 (iketypes.h)
description: Is used to specify various parameters for IPV6 cryptographically generated address (CGA) authentication.
helpviewer_keywords: ["IKEEXT_IPV6_CGA_AUTHENTICATION0","IKEEXT_IPV6_CGA_AUTHENTICATION0 structure [Filtering]","fwp.ikeext_ipv6_cga_authentication0","iketypes/IKEEXT_IPV6_CGA_AUTHENTICATION0"]
old-location: fwp\ikeext_ipv6_cga_authentication0.htm
tech.root: fwp
ms.assetid: 6b472140-f3e3-45b9-81f3-9c428b687fe4
ms.date: 12/05/2018
ms.keywords: IKEEXT_IPV6_CGA_AUTHENTICATION0, IKEEXT_IPV6_CGA_AUTHENTICATION0 structure [Filtering], fwp.ikeext_ipv6_cga_authentication0, iketypes/IKEEXT_IPV6_CGA_AUTHENTICATION0
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: IKEEXT_IPV6_CGA_AUTHENTICATION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_IPV6_CGA_AUTHENTICATION0_
 - iketypes/IKEEXT_IPV6_CGA_AUTHENTICATION0_
 - IKEEXT_IPV6_CGA_AUTHENTICATION0
 - iketypes/IKEEXT_IPV6_CGA_AUTHENTICATION0
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
 - IKEEXT_IPV6_CGA_AUTHENTICATION0
---

# IKEEXT_IPV6_CGA_AUTHENTICATION0 structure


## -description

The <b>IKEEXT_IPV6_CGA_AUTHENTICATION0</b> structure is used to specify various parameters for IPV6 cryptographically generated address (CGA) authentication.

## -struct-fields

### -field keyContainerName

Key container name of the public key/private key pair that was used to generate the CGA.

Same semantics as the <b>pwszContainerName</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure.

### -field cspName

Name of the CSP that stores the key container. If <b>NULL</b>, default provider will be used.

Same semantics as the <b>pwszProvName</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure.

### -field cspType

Type of the CSP that stores the key container.

Same semantics as the <b>dwProvType</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure.

### -field cgaModifier

A [FWP_BYTE_ARRAY16](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array16) structure containing a modifier used during CGA generation.

See CGA RFC for more information.

### -field cgaCollisionCount

Collision count used during CGA generation.

See CGA RFC for more information.

## -remarks

<b>IKEEXT_IPV6_CGA_AUTHENTICATION0</b> is a specific implementation of IKEEXT_IPV6_CGA_AUTHENTICATION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a>



[FWP_BYTE_ARRAY16](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array16)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>