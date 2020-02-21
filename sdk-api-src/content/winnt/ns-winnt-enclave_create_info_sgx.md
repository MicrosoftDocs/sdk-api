---
UID: NS:winnt._ENCLAVE_CREATE_INFO_SGX
title: ENCLAVE_CREATE_INFO_SGX (winnt.h)
description: Contains architecture-specific information to use to create an enclave when the enclave type is ENCLAVE_TYPE_SGX, which specifies an enclave for the Intel Software Guard Extensions (SGX) architecture extension.
old-location: base\enclave_create_info_sgx.htm
tech.root: Memory
ms.assetid: 51ED6E75-DA18-4CCE-8718-46328DD62B07
ms.date: 12/05/2018
ms.keywords: '*PENCLAVE_CREATE_INFO_SGX, ENCLAVE_CREATE_INFO_SGX, ENCLAVE_CREATE_INFO_SGX structure, PENCLAVE_CREATE_INFO_SGX, PENCLAVE_CREATE_INFO_SGX structure pointer, base.enclave_create_info_sgx, winnt/ENCLAVE_CREATE_INFO_SGX, winnt/PENCLAVE_CREATE_INFO_SGX'
f1_keywords:
- winnt/ENCLAVE_CREATE_INFO_SGX
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- winnt.h
api_name:
- ENCLAVE_CREATE_INFO_SGX
targetos: Windows
req.typenames: ENCLAVE_CREATE_INFO_SGX, *PENCLAVE_CREATE_INFO_SGX
req.redist: 
ms.custom: 19H1
---

# ENCLAVE_CREATE_INFO_SGX structure


## -description


Contains architecture-specific information to use to create an enclave when the enclave type is <b>ENCLAVE_TYPE_SGX</b>, which specifies an enclave for the Intel Software Guard Extensions (SGX) architecture extension.


## -struct-fields




### -field Secs

The SGX enclave control structure (<b>SECS</b>) to use to create the enclave.


## -remarks



For more information about the <b>SECS</b> structure, see the Intel SGX Programming Reference that is available from <a href="https://software.intel.com/sgx">Intel Software Guard Extensions</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave">CreateEnclave</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx">ENCLAVE_INIT_INFO_SGX</a>
 

 

