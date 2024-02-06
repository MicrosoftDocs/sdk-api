---
UID: NF:winenclaveapi.EnclaveGetAttestationReport
title: EnclaveGetAttestationReport function (winenclaveapi.h)
description: Gets an enclave attestation report that describes the current enclave and is signed by the authority that is responsible for the type of the enclave.
helpviewer_keywords: ["EnclaveGetAttestationReport","EnclaveGetAttestationReport function","base.enclavegetattestationreport","winenclaveapi/EnclaveGetAttestationReport"]
old-location: base\enclavegetattestationreport.htm
tech.root: base
ms.assetid: FEE8F05B-540F-4C10-A90C-55607A4E9293
ms.date: 02/02/2024
ms.keywords: EnclaveGetAttestationReport, EnclaveGetAttestationReport function, base.enclavegetattestationreport, winenclaveapi/EnclaveGetAttestationReport
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
 - EnclaveGetAttestationReport
 - winenclaveapi/EnclaveGetAttestationReport
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
 - EnclaveGetAttestationReport
---

# EnclaveGetAttestationReport function

## -description

Gets an enclave attestation report that describes the current enclave and is signed by the authority that is responsible for the type of the enclave.

## -parameters

### -param EnclaveData [in, optional]

A pointer to a 64-byte buffer of data that the enclave wants to insert into its signed report.  For example, this buffer could include a 256-bit nonce that the relying party supplied, followed by a SHA-256 hash of additional data that the enclave wants to convey, such as a public key that corresponds to a private key that the enclave owns. If this parameter is `NULL`, the corresponding field of the report is  filled with zeroes.

### -param Report [out]

A pointer to a buffer where the report should be placed. This report may be stored either within the address range of the enclave or within the address space of the host process. Specify `NULL` to indicate that only the size of the buffer required for the output should be calculated, and not the report itself.

### -param BufferSize [in]

The size of the buffer to which the *Report* parameter points. If *Report* is `NULL`, *BufferSize* must be zero. If *Report* is not `NULL`, and if the size of the report is larger than this value, an error is returned.

### -param OutputSize [out]

A pointer to a variable that receives the size of the report.

## -returns

If this function succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

**EnclaveGetAttestationReport** must be called from within an enclave.

**EnclaveGetAttestationReport** is not currently supported for enclaves with a type of **ENCLAVE_TYPE_SGX**. For VBS enclaves, the report that **EnclaveGetAttestationReport** gets is signed by using a VBS-specific key.

The enclave attestation report contains the identity of all code loaded into the enclave, as well as policies that control how the enclave is running, such as whether the enclave is running with debugger access active. The report also includes a small amount of information that the enclave generated to use in a key-exchange protocol.

The report that **EnclaveGetAttestationReport** generates consists of the following items:

- A [VBS_ENCLAVE_REPORT_PKG_HEADER](../ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header.md) structure
- A signed statement that consist of the following items:
  - A [VBS_ENCLAVE_REPORT](../ntenclv/ns-ntenclv-vbs_enclave_report.md) structure
  - Zero or more variable data blocks that consist of the following items:
    - A [VBS_ENCLAVE_REPORT_VARDATA_HEADER](../ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header.md) structure
    - Data described by the [VBS_ENCLAVE_REPORT_VARDATA_HEADER](../ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header.md) structure
- A signature

The enclave attestation report provide proof that specific code is running with an enclave.  If a validating entity  also obtains proof that the host system is running with VBS turned on, that entity can use that proof in conjunction with the enclave attestation report to verify that a specific enclave, populated with specific code, has been loaded.

## -see-also

[Enclave functions](/windows/win32/trusted-execution/enclaves-functions)

[EnclaveVerifyAttestationReport](nf-winenclaveapi-enclaveverifyattestationreport.md)

[VBS_ENCLAVE_REPORT](../ntenclv/ns-ntenclv-vbs_enclave_report.md)

[VBS_ENCLAVE_REPORT_PKG_HEADER](../ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header.md)

[VBS_ENCLAVE_REPORT_VARDATA_HEADER](../ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
