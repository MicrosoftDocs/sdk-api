---
UID: NS:winnt._ENCLAVE_INIT_INFO_SGX
title: ENCLAVE_INIT_INFO_SGX
author: windows-sdk-content
description: Contains architecture-specific information to use to initialize an enclave when the enclave type is ENCLAVE_TYPE_SGX, which specifies an enclave for the Intel Software Guard Extensions (SGX) architecture extension.
old-location: base\enclave_init_info_sgx.htm
tech.root: memory
ms.assetid: A314FF96-A212-4F47-B836-224DE2C3AC0F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PENCLAVE_INIT_INFO_SGX, ENCLAVE_INIT_INFO_SGX, ENCLAVE_INIT_INFO_SGX structure, PENCLAVE_INIT_INFO_SGX, PENCLAVE_INIT_INFO_SGX structure pointer, base.enclave_init_info_sgx, winnt/ENCLAVE_INIT_INFO_SGX, winnt/PENCLAVE_INIT_INFO_SGX"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - ENCLAVE_INIT_INFO_SGX
product: Windows
targetos: Windows
req.typenames: ENCLAVE_INIT_INFO_SGX, *PENCLAVE_INIT_INFO_SGX
req.redist: 
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



For more information about the <b>SIGSTRUCT</b> and <b>EINITTOKEN</b> structures, see the Intel SGX Programming Reference that is available from <a href="https://go.microsoft.com/fwlink/p/?linkid=691175">Intel Software Guard Extensions</a>.




## -see-also




<a href="https://msdn.microsoft.com/51ED6E75-DA18-4CCE-8718-46328DD62B07">ENCLAVE_CREATE_INFO_SGX</a>



<a href="https://msdn.microsoft.com/6A711135-A522-40AE-965F-E1AF97D0076A">InitializeEnclave</a>
 

 

