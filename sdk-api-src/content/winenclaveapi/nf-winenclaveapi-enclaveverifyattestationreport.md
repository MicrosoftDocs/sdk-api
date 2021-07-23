---
UID: NF:winenclaveapi.EnclaveVerifyAttestationReport
title: EnclaveVerifyAttestationReport function (winenclaveapi.h)
description: Verifies an attestation report that was generated on the current system.
helpviewer_keywords: ["EnclaveVerifyAttestationReport","EnclaveVerifyAttestationReport function","base.enclaveverifyattestationreport","winenclaveapi/EnclaveVerifyAttestationReport"]
old-location: base\enclaveverifyattestationreport.htm
tech.root: base
ms.assetid: D74F89FB-9F06-4AA1-9E2E-C9265B3C5B44
ms.date: 12/05/2018
ms.keywords: EnclaveVerifyAttestationReport, EnclaveVerifyAttestationReport function, base.enclaveverifyattestationreport, winenclaveapi/EnclaveVerifyAttestationReport
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
 - EnclaveVerifyAttestationReport
 - winenclaveapi/EnclaveVerifyAttestationReport
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
 - EnclaveVerifyAttestationReport
---

# EnclaveVerifyAttestationReport function


## -description

Verifies an attestation report that was generated on the current system.

## -parameters

### -param EnclaveType [in]

The type of the enclave for which the report was generated. Must be <b>ENCLAVE_TYPE_VBS</b>.

### -param Report [in]

A pointer to a buffer that stores the report.  This report may be stored either within the address range of the enclave or within the address space of the host process.

### -param ReportSize [in]

 The size of the report, in bytes.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is used if two enclaves run on the same system and need to establish a secure channel between one another.  When you call <b>EnclaveVerifyAttestationReport</b> from a virtualization-based security (VBS) enclave, you can only use <b>EnclaveVerifyAttestationReport</b> to validate an attestation report that another VBS enclave generated.

<b>EnclaveVerifyAttestationReport</b> must be called from within an enclave, and is only supported within enclaves that have the  <b>ENCLAVE_TYPE_VBS</b> enclave type.

## -see-also

<a href="/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport">EnclaveGetAttestationReport</a>