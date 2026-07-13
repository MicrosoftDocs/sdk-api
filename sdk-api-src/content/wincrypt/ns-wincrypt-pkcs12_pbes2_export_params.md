---
UID: NS:wincrypt._PKCS12_PBES2_EXPORT_PARAMS
tech.root: security
title: PKCS12_PBES2_EXPORT_PARAMS
ms.date: 10/21/2022
targetos: Windows
description: Passed to the PFXExportCertStoreEx function as pvPara when the PKCS12_EXPORT_PBES2_PARAMS flag is set for dwFlags to provide information about the encryption algorithm to use.
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
req.target-min-winverclnt: Windows 10 1709
req.target-min-winversvr: Windows Server 2019
req.target-type: 
req.typenames: PKCS12_PBES2_EXPORT_PARAMS, *PPKCS12_PBES2_EXPORT_PARAMS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wincrypt.h
api_name:
 - _PKCS12_PBES2_EXPORT_PARAMS
 - PPKCS12_PBES2_EXPORT_PARAMS
 - PKCS12_PBES2_EXPORT_PARAMS
f1_keywords:
 - _PKCS12_PBES2_EXPORT_PARAMS
 - wincrypt/_PKCS12_PBES2_EXPORT_PARAMS
 - PPKCS12_PBES2_EXPORT_PARAMS
 - wincrypt/PPKCS12_PBES2_EXPORT_PARAMS
 - PKCS12_PBES2_EXPORT_PARAMS
 - wincrypt/PKCS12_PBES2_EXPORT_PARAMS
dev_langs:
 - c++
helpviewer_keywords:
 - _PKCS12_PBES2_EXPORT_PARAMS
 - wincrypt/_PKCS12_PBES2_EXPORT_PARAMS
 - PPKCS12_PBES2_EXPORT_PARAMS
 - wincrypt/PPKCS12_PBES2_EXPORT_PARAMS
 - PKCS12_PBES2_EXPORT_PARAMS
 - wincrypt/PKCS12_PBES2_EXPORT_PARAMS
---

## -description

Passed to the [PFXExportCertStoreEx](/windows/win32/api/wincrypt/nf-wincrypt-pfxexportcertstoreex) function as _pvPara_ when the **PKCS12_EXPORT_PBES2_PARAMS** flag is set for _dwFlags_ to provide information about the encryption algorithm to use.

## -struct-fields

### -field dwSize

The size of the structure, in bytes.

### -field hNcryptDescriptor

If the **PKCS12_PROTECT_TO_DOMAIN_SIDS** flag is set for _dwFlags_ when calling the [PFXExportCertStoreEx](/windows/win32/api/wincrypt/nf-wincrypt-pfxexportcertstoreex) function, you can set this field to an **NCRYPT_DESCRIPTOR_HANDLE** value. See the _pvPara_ description in the [PFXExportCertStoreEx](/windows/win32/api/wincrypt/nf-wincrypt-pfxexportcertstoreex) for more information.

### -field pwszPbes2Alg

The designation of the password-based encryption algorithm to use. 

| Value | Meaning |
|-------|---------|
| **PKCS12_PBES2_ALG_AES256_SHA256**</br>AES256-SHA256 | AES256 will be used for key/certificate encryption, and SHA256 will be used for KDF2, and MacData hashing. |

## -remarks

## -see-also

