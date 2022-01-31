---
UID: NE:ntenclv.ENCLAVE_SEALING_IDENTITY_POLICY
title: ENCLAVE_SEALING_IDENTITY_POLICY (ntenclv.h)
description: Defines values that specify how another enclave must be related to the enclave that calls EnclaveSealData for the enclave to unseal the data.
helpviewer_keywords: ["ENCLAVE_IDENTITY_POLICY_SEAL_EXACT_CODE","ENCLAVE_IDENTITY_POLICY_SEAL_INVALID","ENCLAVE_IDENTITY_POLICY_SEAL_SAME_AUTHOR","ENCLAVE_IDENTITY_POLICY_SEAL_SAME_FAMILY","ENCLAVE_IDENTITY_POLICY_SEAL_SAME_IMAGE","ENCLAVE_IDENTITY_POLICY_SEAL_SAME_PRIMARY_CODE","ENCLAVE_SEALING_IDENTITY_POLICY","ENCLAVE_SEALING_IDENTITY_POLICY enumeration","base.enclave_sealing_identity_policy","ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_EXACT_CODE","ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_INVALID","ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_SAME_AUTHOR","ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_SAME_FAMILY","ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_SAME_IMAGE","ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_SAME_PRIMARY_CODE","ntenclv/ENCLAVE_SEALING_IDENTITY_POLICY"]
old-location: base\enclave_sealing_identity_policy.htm
tech.root: base
ms.assetid: 986C122D-4CC9-487F-8B9F-6B3F9B727E4A
ms.date: 12/05/2018
ms.keywords: ENCLAVE_IDENTITY_POLICY_SEAL_EXACT_CODE, ENCLAVE_IDENTITY_POLICY_SEAL_INVALID, ENCLAVE_IDENTITY_POLICY_SEAL_SAME_AUTHOR, ENCLAVE_IDENTITY_POLICY_SEAL_SAME_FAMILY, ENCLAVE_IDENTITY_POLICY_SEAL_SAME_IMAGE, ENCLAVE_IDENTITY_POLICY_SEAL_SAME_PRIMARY_CODE, ENCLAVE_SEALING_IDENTITY_POLICY, ENCLAVE_SEALING_IDENTITY_POLICY enumeration, base.enclave_sealing_identity_policy, ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_EXACT_CODE, ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_INVALID, ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_SAME_AUTHOR, ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_SAME_FAMILY, ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_SAME_IMAGE, ntenclv/ENCLAVE_IDENTITY_POLICY_SEAL_SAME_PRIMARY_CODE, ntenclv/ENCLAVE_SEALING_IDENTITY_POLICY
req.header: ntenclv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
targetos: Windows
req.typenames: ENCLAVE_SEALING_IDENTITY_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ENCLAVE_SEALING_IDENTITY_POLICY
 - ntenclv/ENCLAVE_SEALING_IDENTITY_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntenclv.h
api_name:
 - ENCLAVE_SEALING_IDENTITY_POLICY
---

# ENCLAVE_SEALING_IDENTITY_POLICY enumeration


## -description

Defines values  that specify how another enclave must be related to the enclave that calls <a href="/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata">EnclaveSealData</a> for the enclave to unseal the data.

## -enum-fields

### -field ENCLAVE_IDENTITY_POLICY_SEAL_INVALID:0

This value is not valid. Do not use.

### -field ENCLAVE_IDENTITY_POLICY_SEAL_EXACT_CODE

All of the bytes of every image loaded into the unsealing enclave must match the bytes of every image in the sealing enclave in order for <a href="/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata">EnclaveSealData</a> to decrypt the data.

### -field ENCLAVE_IDENTITY_POLICY_SEAL_SAME_PRIMARY_CODE

All of the bytes of the primary image loaded into the unsealing enclave must match the bytes for the primary image in the sealing enclave in order for <a href="/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata">EnclaveSealData</a> to decrypt the data.

### -field ENCLAVE_IDENTITY_POLICY_SEAL_SAME_IMAGE

The author identifier, family identifier, and image identifier of the primary image of the unsealing enclave must match the author identifier, family identifier, and image identifier of the primary image of the sealing enclave in order for <a href="/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata">EnclaveSealData</a> to decrypt the data. The enclave can be revised by its author as many times as desired, and the data can be unsealed by any enclave with a primary image retains those same identity values.

### -field ENCLAVE_IDENTITY_POLICY_SEAL_SAME_FAMILY

The author identifier and family identifier of the primary image of the unsealing enclave must match the author identifier and family identifier of the primary image of the sealing enclave in order for <a href="/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata">EnclaveSealData</a> to decrypt the data. This case permits an enclave to exchange information with any other enclave in the same family

### -field ENCLAVE_IDENTITY_POLICY_SEAL_SAME_AUTHOR

The author identifier of the primary image of the unsealing enclave must match the author identifier of the primary image of the sealing enclave in order for <a href="/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata">EnclaveSealData</a> to decrypt the data. This case permits an enclave to exchange information with any other enclave generated by the same author.

## -see-also

<a href="/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata">EnclaveSealData</a>
