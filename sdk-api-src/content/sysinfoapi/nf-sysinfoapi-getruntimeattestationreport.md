---
UID: NF:sysinfoapi.GetRuntimeAttestationReport
title: GetRuntimeAttestationReport
ms.date: 01/21/2026
targetos: Windows
description: Retrieve a signed runtime attestation report
prerelease: false
req.construct-type: function
req.dll: Kernel32.dll
req.header: sysinfoapi.h
req.include-header: Windows.h
req.lib: Kernel32.lib
req.target-type: Windows
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sysinfoapi.h
api_name:
 - GetRuntimeAttestationReport
f1_keywords:
 - GetRuntimeAttestationReport
 - sysinfoapi/GetRuntimeAttestationReport
dev_langs:
 - c++
helpviewer_keywords:
 - GetRuntimeAttestationReport
---

## -description

The GetRuntimeAttestationReport API allows a VTL0 user-mode process to retrieve a signed runtime attestation report from the Secure Kernel. This report provides a list of loaded drivers and code integrity information, which is essential for validating system integrity and enforcing anti-cheat policies in gaming and security-sensitive applications.

## -parameters

### -param Nonce

Pointer to a 32-byte buffer containing a nonce to prevent replay attacks. Specify `NULL` if only calculating the output size.

### -param PackageVersion

Specifies the package version of the runtime report. Use `RUNTIME_REPORT_PACKAGE_VERSION_CURRENT` for the latest version.

### -param ReportTypesBitmap

Bitmap specifying the types of reports to generate. Use the `RUNTIME_REPORT_TYPE_TO_MASK` macro to convert enum values to bitmap masks.

* `RuntimeReportTypeDriver` = 0 (driver report)
* `RuntimeReportTypeCodeIntegrity` = 1 (code integrity report)  
* `RUNTIME_REPORT_TYPE_MASK_ALL` (all supported reports)

### -param ReportBuffer

Pointer to a buffer where the signed report will be placed. Specify `NULL` to calculate the required output size only.

### -param ReportBufferSize

Pointer to a variable containing the size of the buffer. Updated with the actual number of bytes written or, if `ReportBuffer` is `NULL`, with the required size.

### -param ReportBufferSize

Pointer to a variable containing the size of the buffer. Updated with the actual number of bytes written or, if ReportBuffer is NULL, with the required size.

## -returns

* Returns TRUE on success.
* Returns FALSE on error; use GetLastError() for extended error information.

## -remarks

The API provides a signed runtime attestation report, which can be validated by the backend.

Call the API periodically during runtime to maintain up-to-date attestation.
Always calculate the required buffer size first by passing NULL for ReportBuffer, then allocate the buffer and call again to retrieve the report.

The report can only be generated when HVCI (Hypervisor-Protected Code Integrity) is enabled.

The returned buffer is organized as a "Runtime Report Package," which includes:

* RUNTIME_REPORT_PACKAGE_HEADER
* 32-byte nonce
* One or more RUNTIME_REPORT_DIGEST_HEADER (one per report type)
* Signature blob
* One or more authenticated runtime reports (each with a RUNTIME_REPORT_HEADER)

### Security Requirements

* TPM 2.0, Secure Boot, VBS, HVCI, and IOMMU must be enabled.
* Test-signing and debug flags must be off.

The attestation report is only valid if these security features are active.

## -see-also

* [GetSystemInfo](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
* [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexw)
* [IsProcessorFeaturePresent](/windows/win32/api/sysinfoapi/nf-sysinfoapi-isprocessorfeaturepresent)
