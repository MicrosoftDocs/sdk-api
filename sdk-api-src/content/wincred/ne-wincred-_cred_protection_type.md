---
UID: NE:wincred._CRED_PROTECTION_TYPE
title: "_CRED_PROTECTION_TYPE"
author: windows-sdk-content
description: Specifies the security context in which credentials are encrypted when using the CredProtect function.
old-location: security\cred_protection_type.htm
old-project: SecAuthN
ms.assetid: 6d8d8ad6-1b44-4482-a9a2-9c50d522b8d9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCRED_PROTECTION_TYPE, CRED_PROTECTION_TYPE, CRED_PROTECTION_TYPE enumeration [Security], CredTrustedProtection, CredUnprotected, CredUserProtection, PCRED_PROTECTION_TYPE, PCRED_PROTECTION_TYPE enumeration pointer [Security], _CRED_PROTECTION_TYPE, security.cred_protection_type, wincred/CRED_PROTECTION_TYPE, wincred/CredTrustedProtection, wincred/CredUnprotected, wincred/CredUserProtection, wincred/PCRED_PROTECTION_TYPE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wincred.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CRED_PROTECTION_TYPE, *PCRED_PROTECTION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinCred.h
api_name:
 - CRED_PROTECTION_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRED_PROTECTION_TYPE enumeration


## -description


The <b>CRED_PROTECTION_TYPE</b> enumeration specifies the security context in which credentials are encrypted when using the <a href="https://msdn.microsoft.com/1e299dfb-2ffe-463c-9e2c-b7774a2216e3">CredProtect</a> function.


## -enum-fields




### -field CredUnprotected

The credentials are not encrypted.


### -field CredUserProtection

The credentials are encrypted and can be decrypted only in the security context in which they were encrypted or in the security context of a trusted component.


### -field CredTrustedProtection

The credentials are encrypted and can only be decrypted by a trusted component.


### -field CredForSystemProtection



