---
UID: NS:ntenclv.ENCLAVE_IDENTITY
title: ENCLAVE_IDENTITY (ntenclv.h)
description: Describes the identity of the primary module of an enclave.
helpviewer_keywords: ["ENCLAVE_FLAG_DYNAMIC_DEBUG_ACTIVE","ENCLAVE_FLAG_DYNAMIC_DEBUG_ENABLED","ENCLAVE_FLAG_FULL_DEBUG_ENABLED","ENCLAVE_IDENTITY","ENCLAVE_IDENTITY structure","base.enclave_identity","ntenclv/ENCLAVE_IDENTITY"]
old-location: base\enclave_identity.htm
tech.root: base
ms.assetid: D584D824-3C86-4BBB-9086-6DBE0290E0A4
ms.date: 02/02/2024
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

The signing level of the primary module for the enclave.

### -field Reserved

Reserved.

## -see-also

[VBS_ENCLAVE_REPORT](ns-ntenclv-vbs_enclave_report.md)

[Enclave Structures](/windows/win32/trusted-execution/enclaves-structures)
