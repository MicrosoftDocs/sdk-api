---
UID: NE:licenseprotection._LicenseProtectionStatus
title: LicenseProtectionStatus (licenseprotection.h)
description: Describes the protection state of a license key.
helpviewer_keywords: ["LicenseProtectionStatus","LicenseProtectionStatus enumeration [Security]","licenseprotection/LicenseProtectionStatus","security.licenseprotectionstatus"]
old-location:
tech.root: security
ms.assetid:
ms.date: 10/06/2026
ms.keywords: LicenseProtectionStatus, LicenseProtectionStatus enumeration [Security], licenseprotection/LicenseProtectionStatus, security.licenseprotectionstatus
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
req.lib:
req.dll:
req.irql:
targetos: Windows
req.typenames: LicenseProtectionStatus
req.redist:
f1_keywords:
 - _LicenseProtectionStatus
 - licenseprotection/_LicenseProtectionStatus
 - LicenseProtectionStatus
 - licenseprotection/LicenseProtectionStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Licenseprotection.h
api_name:
 - LicenseProtectionStatus
---

# LicenseProtectionStatus enumeration

The **LicenseProtectionStatus** enumeration describes the protection state of a license key that's managed through the [RegisterLicenseKeyWithExpiration](nf-licenseprotection-registerlicensekeywithexpiration.md) and [ValidateLicenseKeyProtection](nf-licenseprotection-validatelicensekeyprotection.md) functions.

## Syntax

```cpp
typedef enum _LicenseProtectionStatus {
  Success,
  LicenseKeyNotFound,
  LicenseKeyUnprotected,
  LicenseKeyCorrupted,
  LicenseKeyAlreadyExists
} LicenseProtectionStatus;
```

## Constants

### Success

The operation succeeded and the license key is protected.

### LicenseKeyNotFound

The specified license key wasn't found.

### LicenseKeyUnprotected

The license key exists but isn't currently protected.

### LicenseKeyCorrupted

The stored license key data is corrupted.

### LicenseKeyAlreadyExists

A license key with the same identity is already registered.

## Requirements

| Requirement | Value |
| --- | --- |
| **Minimum supported client** | Windows 10, version 20H2 [desktop apps only] |
| **Minimum supported server** | Windows Server 2025 [desktop apps only] |
| **Header** | `licenseprotection.h` |

## See also

[RegisterLicenseKeyWithExpiration](nf-licenseprotection-registerlicensekeywithexpiration.md)

[ValidateLicenseKeyProtection](nf-licenseprotection-validatelicensekeyprotection.md)
