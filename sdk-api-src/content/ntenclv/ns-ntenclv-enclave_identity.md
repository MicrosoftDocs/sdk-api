---
UID: NS:ntenclv.ENCLAVE_IDENTITY
title: ENCLAVE_IDENTITY (ntenclv.h)
description: Describes the identity of the primary module of an enclave.
helpviewer_keywords: ["ENCLAVE_FLAG_DYNAMIC_DEBUG_ACTIVE","ENCLAVE_FLAG_DYNAMIC_DEBUG_ENABLED","ENCLAVE_FLAG_FULL_DEBUG_ENABLED","ENCLAVE_IDENTITY","ENCLAVE_IDENTITY structure","base.enclave_identity","ntenclv/ENCLAVE_IDENTITY"]
old-location: base\enclave_identity.htm
tech.root: base
ms.assetid: D584D824-3C86-4BBB-9086-6DBE0290E0A4
ms.date: 02/06/2025
ms.keywords: ENCLAVE_FLAG_DYNAMIC_DEBUG_ACTIVE, ENCLAVE_FLAG_DYNAMIC_DEBUG_ENABLED, ENCLAVE_FLAG_FULL_DEBUG_ENABLED, ENCLAVE_IDENTITY, ENCLAVE_IDENTITY structure, base.enclave_identity, ntenclv/ENCLAVE_IDENTITY
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
req.typenames: ENCLAVE_IDENTITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ENCLAVE_IDENTITY
 - ntenclv/ENCLAVE_IDENTITY
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
 - ENCLAVE_IDENTITY
---

# ENCLAVE_IDENTITY structure

## -description

Describes the identity of the primary module of an enclave.

## -struct-fields

### -field OwnerId

The identifier of the owner for the enclave.

### -field UniqueId

The unique identifier of the primary module for the enclave.

### -field AuthorId

The author identifier of the primary module for the enclave.

### -field FamilyId

The family identifier of the primary module for the enclave.

### -field ImageId

The image identifier of the primary module for the enclave.

### -field EnclaveSvn

The security version number of the primary module for the enclave.

### -field SecureKernelSvn

The security version number of the Virtual Secure Mode (VSM) kernel.

### -field PlatformSvn

The security version number of the platform that hosts the enclave.

### -field Flags

Flags that describe the runtime policy for the enclave.

| Value | Meaning |
|-------|---------|
| **ENCLAVE_FLAG_FULL_DEBUG_ENABLED**<br/>`0x00000001` | The enclave supports debugging. |
| **ENCLAVE_FLAG_DYNAMIC_DEBUG_ENABLED**<br/>`0x00000002` | The enclave supports dynamic debugging. |
| **ENCLAVE_FLAG_DYNAMIC_DEBUG_ACTIVE**<br/>`0x00000004` | Dynamic debugging is turned on for the enclave. |

### -field SigningLevel

This is a reserved field and must be set to zero.

### -field EnclaveType

This is a reserved field and must be set to zero.

## -remarks

Each enclave has an **ENCLAVE_IDENTITY** that's configured when the enclave is created and set when the enclave is initialized. It contains several properties which are described below:

| Property | How is this property generated? | What is the value in validating this property |
|----------|---------------------------------|-----------------------------------------------|
| *OwnerId* | Set when the enclave is created ([CreateEnclave](/windows/win32/api/enclaveapi/nf-enclaveapi-createenclave)) and denotes the owner (creator) of the enclave. | Can be used to distinguish between enclaves that were created by the same owner. |
| *UniqueId* | Uniquely measures the entire content of the enclave image. When an enclave’s primary image is loaded, the digest contained in the PKCS#1 portion of the Authenticode signature is captured as the Enclave Unique ID. | Can be used to distinguish the exact instance of a particular enclave, including the properties of the code running inside the enclave and the signer information. |
| *AuthorId* | A publisher may want to use a given certificate for signing different VBS enclaves and still have a different trust relationship from a sealing perspective. The author ID uniquely identifies an enclave publisher. The author ID is a hash of:<br/><br/>- The signer ID<br/>- The OPUS information in the signature (if one exists). This is added via the `signtool.exe` signing infrastructure. For scenarios where third-party submissions are signed by Microsoft, this is also used to distinguish different submitters. | Can be used to distinguish the enclave publisher for signing purposes. |
| *FamilyId* | A unique identifier (GUID) assigned to the enclave by its author. Denotes enclaves of the same family. | Can be used to distinguish between enclaves with the same family. Can be used to enforce import, sealing, etc. operations to enclaves with the same *FamilyId*. |
| *ImageId* | A unique identifier (GUID) assigned to the enclave by its author. | Can be used to distinguish between enclaves with the same image. Can be used to enforce import, sealing, etc. operations to enclaves with the same *ImageId*. |
| *EnclaveSvn* | The security version number of the primary image within the enclave. | Compared against *MinimumSvn* on module import to determine if import is rejected. It's also used in signing operations. |
| *PlatformSvn* | The security version number of the VSM kernel. | No enclave is permitted to unseal any data which was sealed by a later SVN enclave. |
| *Flags* | Flags describing the runtime policy of the enclave:<br/><br/>- **ENCLAVE_FLAG_FULL_DEBUG_ENABLED** - Indicates that the enclave supports debugging.<br/>- **ENCLAVE_FLAG_DYNAMIC_DEBUG_ENABLED** - Indicates that the enclave supports dynamic debugging.<br/>- **ENCLAVE_FLAG_DYNAMIC_DEBUG_ACTIVE** - Indicates that dynamic debugging was activated for the enclave. | Can be used to confirm if the enclave has debugging enabled or if it has been activated. Multiple permutations can be used to validate the state of the enclave. |

## -see-also

[VBS_ENCLAVE_REPORT](ns-ntenclv-vbs_enclave_report.md)

[Enclave Structures](/windows/win32/trusted-execution/enclaves-structures)

[CreateEnclave](/windows/win32/api/enclaveapi/nf-enclaveapi-createenclave)
