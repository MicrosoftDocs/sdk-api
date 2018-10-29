---
UID: NS:winnt._ENCLAVE_CREATE_INFO_SGX
title: "_ENCLAVE_CREATE_INFO_SGX"
author: windows-sdk-content
description: Contains architecture-specific information to use to create an enclave when the enclave type is ENCLAVE_TYPE_SGX, which specifies an enclave for the Intel Software Guard Extensions (SGX) architecture extension.
old-location: base\enclave_create_info_sgx.htm
tech.root: Memory
ms.assetid: 51ED6E75-DA18-4CCE-8718-46328DD62B07
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PENCLAVE_CREATE_INFO_SGX, ENCLAVE_CREATE_INFO_SGX, ENCLAVE_CREATE_INFO_SGX structure, PENCLAVE_CREATE_INFO_SGX, PENCLAVE_CREATE_INFO_SGX structure pointer, _ENCLAVE_CREATE_INFO_SGX, base.enclave_create_info_sgx, winnt/ENCLAVE_CREATE_INFO_SGX, winnt/PENCLAVE_CREATE_INFO_SGX"
ms.prod: windows
ms.technology: windows-sdk
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
 - ENCLAVE_CREATE_INFO_SGX
product: Windows
targetos: Windows
req.typenames: ENCLAVE_CREATE_INFO_SGX, *PENCLAVE_CREATE_INFO_SGX
req.redist: 
---

# _ENCLAVE_CREATE_INFO_SGX structure


## -description


Contains architecture-specific information to use to create an enclave when the enclave type is <b>ENCLAVE_TYPE_SGX</b>, which specifies an enclave for the Intel Software Guard Extensions (SGX) architecture extension.


## -struct-fields




### -field Secs

The SGX enclave control structure (<b>SECS</b>) to use to create the enclave.


## -remarks



For more information about the <b>SECS</b> structure, see the Intel SGX Programming Reference that is available from <a href="https://go.microsoft.com/fwlink/p/?linkid=691175">Intel Software Guard Extensions</a>.




## -see-also




<a href="https://msdn.microsoft.com/2193AE42-D9CC-4A9C-8676-7DE432ED58C3">CreateEnclave</a>



<a href="https://msdn.microsoft.com/A314FF96-A212-4F47-B836-224DE2C3AC0F">ENCLAVE_INIT_INFO_SGX</a>
 

 

