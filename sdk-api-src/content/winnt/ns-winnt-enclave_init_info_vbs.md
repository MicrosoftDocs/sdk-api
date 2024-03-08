---
UID: NS:winnt._ENCLAVE_INIT_INFO_VBS
title: ENCLAVE_INIT_INFO_VBS (winnt.h)
description: Contains architecture-specific information to use to initialize an enclave when the enclave type is ENCLAVE_TYPE_VBS, which specifies a virtualization-based security (VBS) enclave.
helpviewer_keywords: ["*PENCLAVE_INIT_INFO_VBS","ENCLAVE_INIT_INFO_VBS","ENCLAVE_INIT_INFO_VBS structure","PENCLAVE_INIT_INFO_VBS","PENCLAVE_INIT_INFO_VBS structure pointer","base.enclave_init_info_vbs","winnt/ENCLAVE_INIT_INFO_VBS","winnt/PENCLAVE_INIT_INFO_VBS"]
old-location: base\enclave_init_info_vbs.htm
tech.root: base
ms.assetid: 93DA44C6-6776-4682-84C2-347192669C77
ms.date: 02/02/2024
ms.keywords: '*PENCLAVE_INIT_INFO_VBS, ENCLAVE_INIT_INFO_VBS, ENCLAVE_INIT_INFO_VBS structure, PENCLAVE_INIT_INFO_VBS, PENCLAVE_INIT_INFO_VBS structure pointer, base.enclave_init_info_vbs, winnt/ENCLAVE_INIT_INFO_VBS, winnt/PENCLAVE_INIT_INFO_VBS'
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
req.typenames: ENCLAVE_INIT_INFO_VBS, *PENCLAVE_INIT_INFO_VBS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENCLAVE_INIT_INFO_VBS
 - winnt/_ENCLAVE_INIT_INFO_VBS
 - PENCLAVE_INIT_INFO_VBS
 - winnt/PENCLAVE_INIT_INFO_VBS
 - ENCLAVE_INIT_INFO_VBS
 - winnt/ENCLAVE_INIT_INFO_VBS
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
 - ENCLAVE_INIT_INFO_VBS
---

# ENCLAVE_INIT_INFO_VBS structure

## -description

Contains architecture-specific information to use to initialize an enclave when the enclave type is **ENCLAVE_TYPE_VBS**, which specifies a virtualization-based security (VBS) enclave.

## -struct-fields

### -field Length

The total length of the **ENCLAVE_INIT_INFO_VBS** structure, in bytes.

### -field ThreadCount

Upon entry to the [InitializeEnclave](../enclaveapi/nf-enclaveapi-initializeenclave.md) function, specifies the number of threads to create in the enclave. Upon successful return from **InitializeEnclave**, contains the number of threads the function actually created.

## -see-also

[Enclave Structures](/windows/win32/trusted-execution/enclaves-structures)

[InitializeEnclave](../enclaveapi/nf-enclaveapi-initializeenclave.md)
