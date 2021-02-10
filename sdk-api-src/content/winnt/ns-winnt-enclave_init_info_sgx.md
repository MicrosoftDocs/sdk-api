---
UID: NS:winnt._ENCLAVE_INIT_INFO_SGX
title: ENCLAVE_INIT_INFO_SGX (winnt.h)
description: Contains architecture-specific information to use to initialize an enclave when the enclave type is ENCLAVE_TYPE_SGX, which specifies an enclave for the Intel Software Guard Extensions (SGX) architecture extension.
helpviewer_keywords: ["*PENCLAVE_INIT_INFO_SGX","ENCLAVE_INIT_INFO_SGX","ENCLAVE_INIT_INFO_SGX structure","PENCLAVE_INIT_INFO_SGX","PENCLAVE_INIT_INFO_SGX structure pointer","base.enclave_init_info_sgx","winnt/ENCLAVE_INIT_INFO_SGX","winnt/PENCLAVE_INIT_INFO_SGX"]
old-location: base\enclave_init_info_sgx.htm
tech.root: base
ms.assetid: A314FF96-A212-4F47-B836-224DE2C3AC0F
ms.date: 12/05/2018
ms.keywords: '*PENCLAVE_INIT_INFO_SGX, ENCLAVE_INIT_INFO_SGX, ENCLAVE_INIT_INFO_SGX structure, PENCLAVE_INIT_INFO_SGX, PENCLAVE_INIT_INFO_SGX structure pointer, base.enclave_init_info_sgx, winnt/ENCLAVE_INIT_INFO_SGX, winnt/PENCLAVE_INIT_INFO_SGX'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
req.typenames: ENCLAVE_INIT_INFO_SGX, *PENCLAVE_INIT_INFO_SGX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENCLAVE_INIT_INFO_SGX
 - winnt/_ENCLAVE_INIT_INFO_SGX
 - PENCLAVE_INIT_INFO_SGX
 - winnt/PENCLAVE_INIT_INFO_SGX
 - ENCLAVE_INIT_INFO_SGX
 - winnt/ENCLAVE_INIT_INFO_SGX
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
 - _ENCLAVE_INIT_INFO_SGX
 - PENCLAVE_INIT_INFO_SGX
 - ENCLAVE_INIT_INFO_SGX
---

# ENCLAVE_INIT_INFO_SGX structure


## -description

Contains architecture-specific information to use to initialize an enclave when the enclave type is <b>ENCLAVE_TYPE_SGX</b>, which specifies an enclave for the Intel Software Guard Extensions (SGX) architecture extension.

## -struct-fields

### -field SigStruct

The enclave signature structure (<b>SIGSTRUCT</b>) to use  to initialize the enclave. This structure specifies information about the enclave from the enclave signer.

### -field Reserved1

Not used.

### -field EInitToken

The EINIT token structure (<b>EINITTOKEN</b>) to use  to initialize the enclave. The initialization operation uses this structure to verify that the enclave has permission to start.

### -field Reserved2

Not used.

## -remarks

For more information about the <b>SIGSTRUCT</b> and <b>EINITTOKEN</b> structures, see the Intel SGX Programming Reference that is available from <a href="https://software.intel.com/sgx">Intel Software Guard Extensions</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx">ENCLAVE_CREATE_INFO_SGX</a>



<a href="/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave">InitializeEnclave</a>

