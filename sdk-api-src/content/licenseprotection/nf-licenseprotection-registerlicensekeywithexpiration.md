---
UID: NF:licenseprotection.RegisterLicenseKeyWithExpiration
title: RegisterLicenseKeyWithExpiration function (licenseprotection.h)
description: Registers a license key and associates an expiration date with it.
helpviewer_keywords: ["RegisterLicenseKeyWithExpiration","RegisterLicenseKeyWithExpiration function [Security]","licenseprotection/RegisterLicenseKeyWithExpiration","security.registerlicensekeywithexpiration"]
old-location:
tech.root: security
ms.assetid:
ms.date: 10/06/2026
ms.keywords: RegisterLicenseKeyWithExpiration, RegisterLicenseKeyWithExpiration function [Security], licenseprotection/RegisterLicenseKeyWithExpiration, security.registerlicensekeywithexpiration
req.header: licenseprotection.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 11, version 21H2 (10.0; Build 22000) [desktop apps only]
req.target-min-winversvr: Windows Server 2025 [desktop apps only]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib: api-ms-win-security-licenseprotection-l1-1-0.lib
req.dll: Licenseprotection.dll; api-ms-win-security-licenseprotection-l1
req.irql:
targetos: Windows
req.typenames:
req.redist:
f1_keywords:
 - RegisterLicenseKeyWithExpiration
 - licenseprotection/RegisterLicenseKeyWithExpiration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Licenseprotection.dll
 - api-ms-win-security-licenseprotection-l1
api_name:
 - RegisterLicenseKeyWithExpiration
---

# RegisterLicenseKeyWithExpiration function

Registers a license key and associates an expiration date with it.

## Syntax

```cpp
HRESULT RegisterLicenseKeyWithExpiration(
  [in]  PCWSTR                   licenseKey,
  [in]  UINT32                   validityInDays,
  [out] LicenseProtectionStatus *status
);
```

## Parameters

*licenseKey* `[in]`

A pointer to a null-terminated wide-character string that specifies the license key to register.

*validityInDays* `[in]`

Specifies the validity period, in days, of the license key.

*status* `[out]`

A pointer to a [LicenseProtectionStatus](ne-licenseprotection-licenseprotectionstatus.md) value that receives the protection status of the license key.

## Return value

Returns `S_OK` if the function succeeds. Otherwise, it returns an `HRESULT` error code.

| Return code | Description |
| --- | --- |
| `S_OK` | The function succeeded. |
| `E_INVALIDARG` | The *validityInDays* parameter is invalid, or the *status* parameter is `NULL`. |

## Remarks

Use the License Protection APIs to register a license key with an associated expiration date, and later return the status of a previously registered key.

## Requirements

| Requirement | Value |
| --- | --- |
| **Minimum supported client** | Windows 11, version 21H2 [desktop apps only] |
| **Minimum supported server** | Windows Server 2025 [desktop apps only] |
| **Header** | `licenseprotection.h` |
| **Library** | `api-ms-win-security-licenseprotection-l1-1-0.lib` |
| **DLL** | `Licenseprotection.dll`; `api-ms-win-security-licenseprotection-l1` |

## See also

[ValidateLicenseKeyProtection](nf-licenseprotection-validatelicensekeyprotection.md)

[LicenseProtectionStatus](ne-licenseprotection-licenseprotectionstatus.md)
