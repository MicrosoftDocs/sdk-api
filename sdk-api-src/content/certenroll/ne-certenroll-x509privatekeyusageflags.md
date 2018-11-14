---
UID: NE:certenroll.X509PrivateKeyUsageFlags
title: X509PrivateKeyUsageFlags
author: windows-sdk-content
description: Specifies the permitted uses of a private key.
old-location: security\x509privatekeyusageflags.htm
tech.root: SecCertEnroll
ms.assetid: 831c4c07-dc26-420a-ac04-d96248f3fad2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: X509PrivateKeyUsageFlags, X509PrivateKeyUsageFlags enumeration [Security], XCN_NCRYPT_ALLOW_ALL_USAGES, XCN_NCRYPT_ALLOW_DECRYPT_FLAG, XCN_NCRYPT_ALLOW_KEY_AGREEMENT_FLAG, XCN_NCRYPT_ALLOW_SIGNING_FLAG, XCN_NCRYPT_ALLOW_USAGES_NONE, certenroll/X509PrivateKeyUsageFlags, certenroll/XCN_NCRYPT_ALLOW_ALL_USAGES, certenroll/XCN_NCRYPT_ALLOW_DECRYPT_FLAG, certenroll/XCN_NCRYPT_ALLOW_KEY_AGREEMENT_FLAG, certenroll/XCN_NCRYPT_ALLOW_SIGNING_FLAG, certenroll/XCN_NCRYPT_ALLOW_USAGES_NONE, security.x509privatekeyusageflags
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
 - X509PrivateKeyUsageFlags
product: Windows
targetos: Windows
req.typenames: X509PrivateKeyUsageFlags
req.redist: 
---

# X509PrivateKeyUsageFlags enumeration


## -description


The <b>X509PrivateKeyUsageFlags</b> enumeration specifies the permitted uses of a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. It is the responsibility of the cryptographic provider. The enumeration value can be set and retrieved by using the <a href="https://msdn.microsoft.com/e983c95b-6b3a-4e27-8a23-ef9051b11a16">KeyUsage</a> property on the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> interface.


## -enum-fields




### -field XCN_NCRYPT_ALLOW_USAGES_NONE

The permitted uses are not defined.


### -field XCN_NCRYPT_ALLOW_DECRYPT_FLAG

The key can be used to decrypt content. This maps to the following <a href="https://msdn.microsoft.com/3fcb91a3-ffcd-419f-a686-3fd2d1e795b3">X509KeyUsageFlags</a> values:

<ul>
<li>XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>XCN_CERT_DECIPHER_ONLY_KEY_USAGE</li>
<li>XCN_CERT_ENCIPHER_ONLY_KEY_USAGE</li>
<li>XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
</ul>

### -field XCN_NCRYPT_ALLOW_SIGNING_FLAG

The key can be used for signing. This maps to the following <a href="https://msdn.microsoft.com/3fcb91a3-ffcd-419f-a686-3fd2d1e795b3">X509KeyUsageFlags</a> values:

<ul>
<li>XCN_CERT_CRL_SIGN_KEY_USAGE</li>
<li>XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>XCN_CERT_KEY_CERT_SIGN_KEY_USAGE</li>
</ul>

### -field XCN_NCRYPT_ALLOW_KEY_AGREEMENT_FLAG

The key can be used to establish key agreement between entities.


### -field XCN_NCRYPT_ALLOW_KEY_IMPORT_FLAG


### -field XCN_NCRYPT_ALLOW_ALL_USAGES

All of the uses defined for this enumeration are permitted.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

