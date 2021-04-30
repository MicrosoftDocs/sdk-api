---
UID: NS:ipsectypes.IPSEC_SA0_
title: IPSEC_SA0 (ipsectypes.h)
description: Is used to store information about an IPsec security association (SA).
helpviewer_keywords: ["IPSEC_SA0","IPSEC_SA0 structure [Filtering]","fwp.ipsec_sa0_struct","ipsectypes/IPSEC_SA0"]
old-location: fwp\ipsec_sa0_struct.htm
tech.root: fwp
ms.assetid: 9d60f5d7-57af-4c33-90ed-b69a9671a9ce
ms.date: 12/05/2018
ms.keywords: IPSEC_SA0, IPSEC_SA0 structure [Filtering], fwp.ipsec_sa0_struct, ipsectypes/IPSEC_SA0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_SA0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA0_
 - ipsectypes/IPSEC_SA0_
 - IPSEC_SA0
 - ipsectypes/IPSEC_SA0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_SA0
---

# IPSEC_SA0 structure


## -description

The <b>IPSEC_SA0</b> structure is used to store information about an IPsec security association (SA).

## -struct-fields

### -field spi

Security parameter index (SPI) of the IPsec SA. <b>IPSEC_SA_SPI</b> is defined in ipsectypes.h as UINT32.

### -field saTransformType

Transform type of the SA specifying the IPsec security protocol.

See [IPSEC_TRANSFORM_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_transform_type) for more information.

### -field ahInformation

Security algorithms of the SA transform. Available when <b>saTransformType</b> is <b>IPSEC_TRANSFORM_AH</b>.

See [IPSEC_SA_AUTH_INFORMATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0) for more information.

### -field espAuthInformation

Security algorithms of the SA transform. Available when <b>saTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH</b>.

See [IPSEC_SA_AUTH_INFORMATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0) for more information.

### -field espCipherInformation

Security algorithms of the SA transform. Available when <b>saTransformType</b> is <b>IPSEC_TRANSFORM_ESP_CIPHER</b>.

See [IPSEC_SA_CIPHER_INFORMATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0) for more information.

### -field espAuthAndCipherInformation

Security algorithms of the SA transform. Available when <b>saTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH_AND_CIPHER</b>.

See <a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0">IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0</a> for more information.

### -field espAuthFwInformation

Security algorithms of the SA transform. Available when <b>saTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH_FW</b>.


<div class="alert"><b>Note</b>  Available only on Windows Server 2008 R2, Windows 7, or later.</div>
<div> </div>

## -remarks

<b>IPSEC_SA0</b> is a specific implementation of IPSEC_SA. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0">IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0</a>



[IPSEC_SA_AUTH_INFORMATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)



[IPSEC_SA_CIPHER_INFORMATION0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)



[IPSEC_TRANSFORM_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_transform_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>