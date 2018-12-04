---
UID: NE:mfapi._MFSampleEncryptionProtectionScheme
title: "_MFSampleEncryptionProtectionScheme"
author: windows-sdk-content
description: Specifies the supported protection schemes for encrypted samples.
old-location: mf\mfsampleencryptionprotectionscheme.htm
tech.root: medfound
ms.assetid: 2FD4ABDA-ED8D-4403-955B-3BCEEA3C8BE7
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: MFSampleEncryptionProtectionScheme, MFSampleEncryptionProtectionScheme enumeration [Media Foundation], SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC, SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CTR, SAMPLE_ENCRYPTION_PROTECTION_SCHEME_NONE, _MFSampleEncryptionProtectionScheme, mf.mfsampleencryptionprotectionscheme, mfapi/MFSampleEncryptionProtectionScheme, mfapi/SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC, mfapi/SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CTR, mfapi/SAMPLE_ENCRYPTION_PROTECTION_SCHEME_NONE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFSampleEncryptionProtectionScheme
product: Windows
targetos: Windows
req.typenames: MFSampleEncryptionProtectionScheme
req.redist: 
---

# _MFSampleEncryptionProtectionScheme enumeration


## -description


Specifies the supported protection schemes for encrypted samples.


## -enum-fields




### -field MF_SAMPLE_ENCRYPTION_PROTECTION_SCHEME_NONE


### -field MF_SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CTR


### -field MF_SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC




#### - SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC

The encryption scheme is Cipher Block Chaining (CBC).


#### - SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CTR

The encryption scheme is AES counter mode (CTR).


#### - SAMPLE_ENCRYPTION_PROTECTION_SCHEME_NONE

No encryption scheme.


## -remarks



The encryption scheme for a sample is specified using the <a href="https://msdn.microsoft.com/04E9F908-C61C-43DC-8CF5-9A629FCDD82C">MFSampleExtension_Encryption_ProtectionScheme</a> attribute.



