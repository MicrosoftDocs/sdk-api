---
UID: NE:mfapi._MFSampleEncryptionProtectionScheme
title: MFSampleEncryptionProtectionScheme (mfapi.h)
description: Specifies the supported protection schemes for encrypted samples.
helpviewer_keywords: ["MFSampleEncryptionProtectionScheme","MFSampleEncryptionProtectionScheme enumeration [Media Foundation]","SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC","SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CTR","SAMPLE_ENCRYPTION_PROTECTION_SCHEME_NONE","mf.mfsampleencryptionprotectionscheme","mfapi/MFSampleEncryptionProtectionScheme","mfapi/SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC","mfapi/SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CTR","mfapi/SAMPLE_ENCRYPTION_PROTECTION_SCHEME_NONE"]
old-location: mf\mfsampleencryptionprotectionscheme.htm
tech.root: mf
ms.assetid: 2FD4ABDA-ED8D-4403-955B-3BCEEA3C8BE7
ms.date: 12/05/2018
ms.keywords: MFSampleEncryptionProtectionScheme, MFSampleEncryptionProtectionScheme enumeration [Media Foundation], SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC, SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CTR, SAMPLE_ENCRYPTION_PROTECTION_SCHEME_NONE, mf.mfsampleencryptionprotectionscheme, mfapi/MFSampleEncryptionProtectionScheme, mfapi/SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC, mfapi/SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CTR, mfapi/SAMPLE_ENCRYPTION_PROTECTION_SCHEME_NONE
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: MFSampleEncryptionProtectionScheme
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFSampleEncryptionProtectionScheme
 - mfapi/_MFSampleEncryptionProtectionScheme
 - MFSampleEncryptionProtectionScheme
 - mfapi/MFSampleEncryptionProtectionScheme
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFSampleEncryptionProtectionScheme
---

## -description

Specifies the supported protection schemes for encrypted samples.

## -enum-fields

### -field MF_SAMPLE_ENCRYPTION_PROTECTION_SCHEME_NONE:0

No encryption scheme.

### -field MF_SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CTR:1

The encryption scheme is AES counter mode (CTR).

### -field MF_SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC:2

The encryption scheme is Cipher Block Chaining (CBC).

## -remarks

The encryption scheme for a sample is specified using the <a href="/windows/desktop/medfound/mfsampleextension-encryption-protectionscheme">MFSampleExtension_Encryption_ProtectionScheme</a> attribute.
