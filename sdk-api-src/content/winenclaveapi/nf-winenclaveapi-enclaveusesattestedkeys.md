---
UID: NF:winenclaveapi.EnclaveUsesAttestedKeys
tech.root: base
title: EnclaveUsesAttestedKeys function (winenclaveapi.h)
ms.date: 04/24/2025
targetos: Windows
description: This method indicates whether the Enclave uses safe attested keys.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Vertdll.dll
req.header: winenclaveapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Vertdll.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 24H2 [desktop apps only]
req.target-min-winversvr: Windows Server 2025 [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winenclaveapi.h
api_name:
 - EnclaveUsesAttestedKeys
f1_keywords:
 - EnclaveUsesAttestedKeys
 - winenclaveapi/EnclaveUsesAttestedKeys
dev_langs:
 - c++
helpviewer_keywords:
 - EnclaveUsesAttestedKeys
---

## -description

This method returns whether the Enclave uses safe attested keys.

## -returns

A **BOOLEAN** value set to `true` if the Enclave uses safe attested keys.

## -remarks

Since remote attestation of the Master key is still not supported the function verifies that:

- No Boot, Kernel or Hypervisor Debugger is ever enabled (which can interfere with the secure keys).
- The Master and encryption keys are safely provisioned by the Trusted Platform Module (TPM).

## -see-also
