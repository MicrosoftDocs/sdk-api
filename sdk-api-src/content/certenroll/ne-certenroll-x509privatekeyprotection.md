---
UID: NE:certenroll.X509PrivateKeyProtection
title: X509PrivateKeyProtection
author: windows-sdk-content
description: Specifies the level of private key protection supported by a cryptographic provider.
old-location: security\x509privatekeyprotection.htm
tech.root: SecCertEnroll
ms.assetid: 70f398bc-95bf-459c-901c-d829946aedca
ms.author: windowssdkdev
ms.date: 09/26/2018
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X509PrivateKeyProtection
product: Windows
targetos: Windows
req.typenames: X509PrivateKeyProtection
req.redist: 
---

# X509PrivateKeyProtection enumeration


## -description


The <b>X509PrivateKeyProtection</b> enumeration specifies the level of <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> protection supported by a cryptographic  provider. For example, if strong key protection is enabled, the user is typically prompted to enter a password when the key is created and whenever the key is used. The precise behavior is specified by the KSP or CSP being used. The  enumeration value can be specified or retrieved by using the <a href="https://msdn.microsoft.com/en-us/library/Aa379019(v=VS.85).aspx">KeyProtection</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> interface.


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




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
 

 

