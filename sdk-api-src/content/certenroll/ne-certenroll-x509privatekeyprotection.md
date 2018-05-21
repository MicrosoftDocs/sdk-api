---
UID: NE:certenroll.X509PrivateKeyProtection
title: X509PrivateKeyProtection
author: windows-driver-content
description: Specifies the level of private key protection supported by a cryptographic provider.
old-location: security\x509privatekeyprotection.htm
old-project: SecCertEnroll
ms.assetid: 70f398bc-95bf-459c-901c-d829946aedca
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: X509PrivateKeyProtection, X509PrivateKeyProtection enumeration [Security], XCN_NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG, XCN_NCRYPT_UI_NO_PROTECTION_FLAG, XCN_NCRYPT_UI_PROTECT_KEY_FLAG, certenroll/X509PrivateKeyProtection, certenroll/XCN_NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG, certenroll/XCN_NCRYPT_UI_NO_PROTECTION_FLAG, certenroll/XCN_NCRYPT_UI_PROTECT_KEY_FLAG, security.x509privatekeyprotection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: X509PrivateKeyProtection
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CertEnroll.h
api_name:
-	X509PrivateKeyProtection
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509PrivateKeyProtection enumeration


## -description


The <b>X509PrivateKeyProtection</b> enumeration specifies the level of <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> protection supported by a cryptographic  provider. For example, if strong key protection is enabled, the user is typically prompted to enter a password when the key is created and whenever the key is used. The precise behavior is specified by the KSP or CSP being used. The  enumeration value can be specified or retrieved by using the <a href="https://msdn.microsoft.com/39d8b9ac-ebbd-4bd8-8d5e-a4b28595b030">KeyProtection</a> property on the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> interface.


## -enum-fields




### -field XCN_NCRYPT_UI_NO_PROTECTION_FLAG

The protection level is not specified.


### -field XCN_NCRYPT_UI_PROTECT_KEY_FLAG

A user interface is displayed to indicate that a process is attempting to use the key. The exact behavior is specified by the KSP or CSP being used. Some Microsoft legacy CSPs allow the client to decide whether a password is required to use the key or whether the user must only acknowledge a prompt.


### -field XCN_NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG

Specifies strong key protection. The user is typically prompted to enter a password when the key is created and whenever the key is used. The exact behavior is specified by the KSP being used. This value is not supported by the Certificate Enrollment API for legacy CSPs.


### -field XCN_NCRYPT_UI_FINGERPRINT_PROTECTION_FLAG


### -field XCN_NCRYPT_UI_APPCONTAINER_ACCESS_MEDIUM_FLAG




## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

