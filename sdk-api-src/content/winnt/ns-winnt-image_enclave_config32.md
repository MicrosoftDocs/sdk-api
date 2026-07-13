---
UID: NS:winnt._IMAGE_ENCLAVE_CONFIG32
title: IMAGE_ENCLAVE_CONFIG32 (winnt.h)
description: Defines the format of the enclave configuration for systems running 32-bit Windows. (32 bit)
helpviewer_keywords: ["*PIMAGE_ENCLAVE_CONFIG32","IMAGE_ENCLAVE_CONFIG","IMAGE_ENCLAVE_CONFIG32","IMAGE_ENCLAVE_CONFIG32 structure","IMAGE_ENCLAVE_FLAG_PRIMARY_IMAGE","IMAGE_ENCLAVE_POLICY_DEBUGGABLE","PIMAGE_ENCLAVE_CONFIG32","PIMAGE_ENCLAVE_CONFIG32 structure pointer","_IMAGE_ENCLAVE_CONFIG32","base.image_enclave_config","base.image_enclave_config32","winnt/IMAGE_ENCLAVE_CONFIG32","winnt/PIMAGE_ENCLAVE_CONFIG32"]
old-location: base\image_enclave_config32.htm
tech.root: base
ms.assetid: 6006F018-4F3F-4595-8ED2-89D2CC7F782D
ms.date: 02/02/2024
ms.keywords: '*PIMAGE_ENCLAVE_CONFIG32, IMAGE_ENCLAVE_CONFIG, IMAGE_ENCLAVE_CONFIG32, IMAGE_ENCLAVE_CONFIG32 structure, IMAGE_ENCLAVE_FLAG_PRIMARY_IMAGE, IMAGE_ENCLAVE_POLICY_DEBUGGABLE, PIMAGE_ENCLAVE_CONFIG32, PIMAGE_ENCLAVE_CONFIG32 structure pointer, _IMAGE_ENCLAVE_CONFIG32, base.image_enclave_config, base.image_enclave_config32, winnt/IMAGE_ENCLAVE_CONFIG32, winnt/PIMAGE_ENCLAVE_CONFIG32'
req.header: winnt.h
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
req.typenames: IMAGE_ENCLAVE_CONFIG32, *PIMAGE_ENCLAVE_CONFIG32
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAGE_ENCLAVE_CONFIG32
 - winnt/_IMAGE_ENCLAVE_CONFIG32
 - PIMAGE_ENCLAVE_CONFIG32
 - winnt/PIMAGE_ENCLAVE_CONFIG32
 - IMAGE_ENCLAVE_CONFIG32
 - winnt/IMAGE_ENCLAVE_CONFIG32
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - IMAGE_ENCLAVE_CONFIG32
 - IMAGE_ENCLAVE_CONFIG
---

# IMAGE_ENCLAVE_CONFIG32 structure

## -description

Defines the format of the enclave configuration for systems running 32-bit Windows.

## -struct-fields

### -field Size

The size of the **IMAGE_ENCLAVE_CONFIG32** structure, in bytes.

### -field MinimumRequiredConfigSize

The minimum size of the **IMAGE_ENCLAVE_CONFIG32** structure that the image loader must be able to process in order for the enclave to be usable. This member allows an enclave to inform an earlier version of the image loader that the image loader can safely load the enclave and ignore optional members added to **IMAGE_ENCLAVE_CONFIG32** for later versions of the enclave. If the size of **IMAGE_ENCLAVE_CONFIG32** that the image loader can process is less than **MinimumRequiredConfigSize**, the enclave cannot be run securely.

If **MinimumRequiredConfigSize** is zero, the minimum size of the **IMAGE_ENCLAVE_CONFIG32** structure that the image loader must be able to process in order for the enclave to be usable is assumed to be the size of the structure through and including the **MinimumRequiredConfigSize** member.

### -field PolicyFlags

Flags that indicate the policies that have been set for the enclave. These flags can be set to indicate whether the enclave permits debugging and whether the enclave is restricted to using its own memory space.

| Value | Meaning |
|-------|---------|
| `0x00000000` | The enclave does not permit debugging. |
| **IMAGE_ENCLAVE_POLICY_DEBUGGABLE**<br/>`0x00000001` | The enclave permits debugging. |
| **IMAGE_ENCLAVE_POLICY_STRICT_MEMORY**<br/>`0x00000002` | This flag restricts access by an enclave to the address space of its containing process. This policy applies to all threads in the enclave. The enclave must use the [EnclaveCopyIntoEnclave](../winenclaveapi/nf-winenclaveapi-enclavecopyintoenclave.md) and [EnclaveCopyOutOfEnclave](../winenclaveapi/nf-winenclaveapi-enclavecopyoutofenclave.md) APIs to access containing process memory.<br/><br/>**Note:** Access to the containing process's address space can also be restricted by calling the [EnclaveRestrictContainingProcessAccess](../winenclaveapi/nf-winenclaveapi-enclaverestrictcontainingprocessaccess.md) API. This API can also be used to relax this policy at runtime and restore access to the containing process memory. |

### -field NumberOfImports

The number of images in the array of images that the **ImportList** member points to.

### -field ImportList

The relative virtual address of the array of images that the enclave image may import, with identity information for each image.

### -field ImportEntrySize

The size of each image in the array of images that the **ImportList** member points to.

### -field FamilyID

The family identifier that the author of the enclave assigned to the enclave.

### -field ImageID

The image identifier that the author of the enclave assigned to the enclave.

### -field ImageVersion

The version number that the author of the enclave assigned to the enclave.

### -field SecurityVersion

The security version number that the author of the enclave assigned to the enclave.

### -field EnclaveSize

The expected virtual size of the private address range for the enclave, in bytes.

### -field NumberOfThreads

The maximum number of threads that can be created within the enclave.

### -field EnclaveFlags

A flag that indicates whether the image is suitable for use as the primary image in the enclave.

| Value | Meaning |
|-------|---------|
| `0x00000000` | The image is not suitable for use as the primary image in the enclave. |
| **IMAGE_ENCLAVE_FLAG_PRIMARY_IMAGE**<br/>`0x00000001` | The image is suitable for use as the primary image in the enclave. |

## -remarks

The **IMAGE_ENCLAVE_CONFIG** structure is defined as another name for the **IMAGE_ENCLAVE_CONFIG32** structure on systems that run 32-bit Windows.

## -see-also

[Enclave Structures](/windows/win32/trusted-execution/enclaves-structures)

[IMAGE_ENCLAVE_CONFIG64](ns-winnt-image_enclave_config64.md)

[EnclaveCopyIntoEnclave](../winenclaveapi/nf-winenclaveapi-enclavecopyintoenclave.md)

[EnclaveCopyOutOfEnclave](../winenclaveapi/nf-winenclaveapi-enclavecopyoutofenclave.md)

[EnclaveRestrictContainingProcessAccess](../winenclaveapi/nf-winenclaveapi-enclaverestrictcontainingprocessaccess.md)
