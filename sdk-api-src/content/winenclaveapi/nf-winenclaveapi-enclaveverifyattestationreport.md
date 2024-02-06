---
UID: NF:winenclaveapi.EnclaveVerifyAttestationReport
title: EnclaveVerifyAttestationReport function (winenclaveapi.h)
description: Verifies an attestation report that was generated on the current system.
helpviewer_keywords: ["EnclaveVerifyAttestationReport","EnclaveVerifyAttestationReport function","base.enclaveverifyattestationreport","winenclaveapi/EnclaveVerifyAttestationReport"]
old-location: base\enclaveverifyattestationreport.htm
tech.root: base
ms.assetid: D74F89FB-9F06-4AA1-9E2E-C9265B3C5B44
ms.date: 02/02/2024
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

The type of the enclave for which the report was generated. Must be **ENCLAVE_TYPE_VBS**.

### -param Report [in]

A pointer to a buffer that stores the report.  This report may be stored either within the address range of the enclave or within the address space of the host process.

### -param ReportSize [in]

The size of the report, in bytes.

## -returns

If this function succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

This function is used if two enclaves run on the same system and need to establish a secure channel between one another.  When you call **EnclaveVerifyAttestationReport** from a virtualization-based security (VBS) enclave, you can only use **EnclaveVerifyAttestationReport** to validate an attestation report that another VBS enclave generated.

**EnclaveVerifyAttestationReport** must be called from within an enclave, and is only supported within enclaves that have the  **ENCLAVE_TYPE_VBS** enclave type.

## -see-also

[Enclave functions](/windows/win32/trusted-execution/enclaves-functions)

[EnclaveGetAttestationReport](nf-winenclaveapi-enclavegetattestationreport.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
