---
UID: NF:winenclaveapi.EnclaveGetEnclaveInformation
title: EnclaveGetEnclaveInformation function (winenclaveapi.h)
description: Gets information about the currently executing enclave.
helpviewer_keywords: ["EnclaveGetEnclaveInformation","EnclaveGetEnclaveInformation function","base.enclavegetenclaveinformation","winenclaveapi/EnclaveGetEnclaveInformation"]
old-location: base\enclavegetenclaveinformation.htm
tech.root: base
ms.assetid: 26349C3C-4B73-430C-B002-ED262DB0304F
ms.date: 12/05/2018
ms.keywords: EnclaveGetEnclaveInformation, EnclaveGetEnclaveInformation function, base.enclavegetenclaveinformation, winenclaveapi/EnclaveGetEnclaveInformation
req.header: winenclaveapi.h
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
req.lib: Vertdll.lib
req.dll: Vertdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnclaveGetEnclaveInformation
 - winenclaveapi/EnclaveGetEnclaveInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - vertdll.dll
api_name:
 - EnclaveGetEnclaveInformation
---

# EnclaveGetEnclaveInformation function


## -description

Gets information about the currently executing enclave.

## -parameters

### -param InformationSize [in]

The size of the <a href="/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information">ENCLAVE_INFORMATION</a> structure that the <i>EnclaveInformation</i> parameter points to, in bytes.

### -param EnclaveInformation [out]

Information about the currently executing enclave.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>EnclaveGetEnclaveInformation</b> must be called from within an enclave, and is only supported within enclaves that have the  <b>ENCLAVE_TYPE_VBS</b> enclave type.

## -see-also

<a href="/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information">ENCLAVE_INFORMATION</a>