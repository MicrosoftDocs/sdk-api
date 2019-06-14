---
UID: NS:mprapi._ROUTER_CUSTOM_IKEv2_POLICY0
title: ROUTER_CUSTOM_IKEv2_POLICY0 (mprapi.h)
author: windows-sdk-content
description: Contains the IKEv2 main mode and quick mode policy configuration.
old-location: rras\router_custom_ikev2_policy0.htm
tech.root: RRAS
ms.assetid: 46ea7b05-0d2d-4ba1-b3c3-fab67eabf552
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PROUTER_CUSTOM_IKEv2_POLICY0, *PROUTER_CUSTOM_L2TP_POLICY0, PROUTER_CUSTOM_IKEv2_POLICY0, PROUTER_CUSTOM_IKEv2_POLICY0 structure pointer [RAS], ROUTER_CUSTOM_IKEv2_POLICY0, ROUTER_CUSTOM_IKEv2_POLICY0 structure [RAS], ROUTER_CUSTOM_L2TP_POLICY0, mprapi/PROUTER_CUSTOM_IKEv2_POLICY0, mprapi/ROUTER_CUSTOM_IKEv2_POLICY0, rras.router_custom_ikev2_policy0"
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mprapi.h
api_name:
 - ROUTER_CUSTOM_IKEv2_POLICY0
product: Windows
targetos: Windows
req.typenames: ROUTER_CUSTOM_IKEv2_POLICY0, *PROUTER_CUSTOM_IKEv2_POLICY0, ROUTER_CUSTOM_L2TP_POLICY0, *PROUTER_CUSTOM_L2TP_POLICY0
req.redist: 
ms.custom: 19H1
---

# ROUTER_CUSTOM_IKEv2_POLICY0 structure


## -description


Contains the IKEv2 main mode and quick mode policy configuration.

Do not use the  <b>ROUTER_CUSTOM_IKEv2_POLICY0</b> structure directly in your code; using <a href="https://docs.microsoft.com/windows/desktop/RRAS/router-management-data-types">ROUTER_CUSTOM_IKEv2_POLICY</a> instead ensures that the proper version, based on the operating system the code in compiled under, is used.


## -struct-fields




### -field dwIntegrityMethod

A value that specifies the integrity algorithm to be negotiated during IKEv2 main mode SA negotiation. The allowed values for this member are defined in <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_integrity_type_">IKEEXT_INTEGRITY_TYPE</a>.


### -field dwEncryptionMethod

A value that specifies the encryption algorithm to be negotiated during IKEv2 main mode SA negotiation. The allowed valued for this member are defined in <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_cipher_type_">IKEEXT_CIPHER_TYPE</a>.


### -field dwCipherTransformConstant

A value that specifies the encryption algorithm to be negotiated during IKEv2 quick mode SA negotiation. The allowed valued for this member are defined in <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_cipher_type_">IPSEC_CIPHER_TYPE</a>.


### -field dwAuthTransformConstant

A value that specifies the hash algorithm to be negotiated during IKEv2 quick mode SA negotiation. The allowed valued for this member are defined in <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_auth_type_">IPSEC_AUTH_TYPE</a>.


### -field dwPfsGroup

A value that specifies the Diffie Hellman algorithm that should be used for Quick Mode PFS (Perfect Forward Secrecy). The allowed valued for this member are defined in <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_pfs_group_">IPSEC_PFS_GROUP</a>.


### -field dwDhGroup

A value that specifies the type of Diffie Hellman group used for Internet Key Exchange (IKE) key generation during MM SA negotiation. The allowed valued for this member are defined in <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_dh_group_">IKEEXT_DH_GROUP</a>.

