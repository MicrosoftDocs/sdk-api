---
UID: NF:licenseprotection.ValidateLicenseKeyProtection
title: ValidateLicenseKeyProtection function (licenseprotection.h)
description: Validates a license key that was previously registered and returns its validity period and protection status.
helpviewer_keywords: ["ValidateLicenseKeyProtection","ValidateLicenseKeyProtection function [Security]","licenseprotection/ValidateLicenseKeyProtection","security.validatelicensekeyprotection"]
old-location:
tech.root: security
ms.assetid:
ms.date: 10/06/2026
ms.keywords: ValidateLicenseKeyProtection, ValidateLicenseKeyProtection function [Security], licenseprotection/ValidateLicenseKeyProtection, security.validatelicensekeyprotection
req.header: licenseprotection.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 20H2 (10.0; Build 19042) [desktop apps only]
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
 - ValidateLicenseKeyProtection
 - licenseprotection/ValidateLicenseKeyProtection
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
 - ValidateLicenseKeyProtection
---

# ValidateLicenseKeyProtection function

Validates a license key that was previously registered and returns when it is valid and its protection status.

## Syntax

```cpp
HRESULT ValidateLicenseKeyProtection(
  [in]  PCWSTR                   licenseKey,
  [out] PFILETIME                notValidBefore,
  [out] PFILETIME                notValidAfter,
  [out] LicenseProtectionStatus *status
);
```

## Parameters

*licenseKey* `[in]`

A pointer to a null-terminated wide-character string that specifies the license key to validate.

*notValidBefore* `[out]`

A pointer to a `FILETIME` structure that receives the date and time before which the license key isn't valid.

*notValidAfter* `[out]`

A pointer to a `FILETIME` structure that receives the date and time after which the license key isn't valid.

*status* `[out]`

A pointer to a [LicenseProtectionStatus](ne-licenseprotection-licenseprotectionstatus.md) value that receives the protection status of the license key.

## Return value

Returns `S_OK` if the function succeeds. Otherwise, it returns an `HRESULT` error code.

| Return code | Description |
| --- | --- |
| `S_OK` | The function succeeded. |
| `E_INVALIDARG` | One or more of the parameters is `NULL`. |

## Remarks

Use [RegisterLicenseKeyWithExpiration](nf-licenseprotection-registerlicensekeywithexpiration.md) to register a license key before calling **ValidateLicenseKeyProtection**.

## Requirements

| Requirement | Value |
| --- | --- |
| **Minimum supported client** | Windows 10, version 20H2 [desktop apps only] |
| **Minimum supported server** | Windows Server 2025 [desktop apps only] |
| **Header** | `licenseprotection.h` |
| **Library** | `api-ms-win-security-licenseprotection-l1-1-0.lib` |
| **DLL** | `Licenseprotection.dll`; `api-ms-win-security-licenseprotection-l1` |

## See also

[RegisterLicenseKeyWithExpiration](nf-licenseprotection-registerlicensekeywithexpiration.md)

[LicenseProtectionStatus](ne-licenseprotection-licenseprotectionstatus.md)
