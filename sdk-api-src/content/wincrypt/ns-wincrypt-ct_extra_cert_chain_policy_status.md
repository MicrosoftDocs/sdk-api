---
UID: NS:wincrypt._CT_EXTRA_CERT_CHAIN_POLICY_STATUS
tech.root: security
title: CT_EXTRA_CERT_CHAIN_POLICY_STATUS
ms.date: 05/16/2025
targetos: Windows
description: The struct contains extra error information about the status of a Certificate Transparency chain policy check.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: wincrypt.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 11 [desktop apps only]
req.target-min-winversvr: Windows Server 2022 [desktop apps only]
req.assembly: 
req.type-library:
req.target-type: 
req.typenames: CT_EXTRA_CERT_CHAIN_POLICY_STATUS, *PCT_EXTRA_CERT_CHAIN_POLICY_STATUS
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wincrypt.h
api_name:
 - _CT_EXTRA_CERT_CHAIN_POLICY_STATUS
 - PCT_EXTRA_CERT_CHAIN_POLICY_STATUS
 - CT_EXTRA_CERT_CHAIN_POLICY_STATUS
f1_keywords:
 - _CT_EXTRA_CERT_CHAIN_POLICY_STATUS
 - wincrypt/_CT_EXTRA_CERT_CHAIN_POLICY_STATUS
 - PCT_EXTRA_CERT_CHAIN_POLICY_STATUS
 - wincrypt/PCT_EXTRA_CERT_CHAIN_POLICY_STATUS
 - CT_EXTRA_CERT_CHAIN_POLICY_STATUS
 - wincrypt/CT_EXTRA_CERT_CHAIN_POLICY_STATUS
dev_langs:
 - c++
helpviewer_keywords:
 - _CT_EXTRA_CERT_CHAIN_POLICY_STATUS
---

## -description

Contains extra error information about the status of a Certificate Transparency chain policy check.

## -struct-fields

### -field cbSize

The size of the structure, in bytes.

### -field lErrorStatus

The error status of the certificate chain policy.

| Value  | Description                                                              |
|--------|--------------------------------------------------------------------------|
| `> 0`  | Warning - These errors can be ignored. Will map to **S_FALSE**.          |
| `== 0` | Success - Will map to **S_OK**.                                          |
| `< 0 ` | Fatal error - These errors shouldn't be ignored. Will map to **E_FAIL**. |

See [Remarks](#remarks) for more information.

### -field lErrorSubStatus

The substatus of the certificate chain policy. Depends on **lErrorStatus**. Can override **lErrorStatus**.

See [Remarks](#remarks) for more information.

### -field cEntries

The number of SCT entries in the certificate chain.

### -field cValidated

Indicates the number of SCT entries that have been successfully validated in the certificate chain.

## -remarks

The following values are possible **lErrorStatus** and **lErrorSubStatus** fields:

| Value | Description |
|-------|-------------|
| **CERT_CHAIN_POLICY_CT_ERROR_UNDECODABLE_SCT_EXTENSION**<br/>`-112` | SCT extension could not be ASN.1 decoded (invalid syntax or not supported). |
| **CERT_CHAIN_POLICY_CT_ERROR_UNRETRIEVABLE_SCT_EXTENSION**<br/>`-111` | SCT extension could not be retrieved. |
| **CERT_CHAIN_POLICY_CT_ERROR_MISSING_SCT_EXTENSION**<br/>`-110` | SCT extension is missing. |
| **CERT_CHAIN_POLICY_CT_ERROR_INVALID_ISSUER_CERT**<br/>`-101` | The issuer cert could not be converted to the proper format (invalid syntax). |
| **CERT_CHAIN_POLICY_CT_ERROR_INVALID_SUBJECT_CERT**<br/>`-100` | The subject cert could not be converted to the proper format (invalid syntax). |
| **CERT_CHAIN_POLICY_CT_ERROR_SCT_VALIDATION_STATUS_INSUFFICIENT**<br/>`-4` | One or more SCTs were validated but the total valid amount required to pass the CT policy check was not met. |
| **CERT_CHAIN_POLICY_CT_ERROR_SCT_VALIDATION_STATUS_UNKNOWN_VERSION**<br/>`-3` | The SCT is of an unsupported version (only v1 is supported). |
| **CERT_CHAIN_POLICY_CT_ERROR_SCT_VALIDATION_STATUS_UNKNOWN_LOG**<br/>`-2` | The SCT was issued by a log that was not in the CT Log Store. |
| **CERT_CHAIN_POLICY_CT_ERROR_SCT_VALIDATION_STATUS_INVALID**<br/>`-1` | The SCT's signature is incorrect, its timestamp is in the future), or if it is otherwise invalid. |
| **CERT_CHAIN_POLICY_CT_SUCCESS_SCT_VALIDIDATION_STATUS_VALID**<br/>`0` | The amount of valid SCTs required to pass the CT policy check was met. |

## -see-also

[CERT_CHAIN_POLICY_STATUS](ns-wincrypt-cert_chain_policy_status.md)
