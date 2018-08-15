---
UID: NE:certenroll.X509KeyUsageFlags
title: X509KeyUsageFlags
author: windows-sdk-content
description: Specifies the purpose of a key contained in a certificate.
old-location: security\x509keyusageflags_enum.htm
old-project: seccertenroll
ms.assetid: 3fcb91a3-ffcd-419f-a686-3fd2d1e795b3
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: X509KeyUsageFlags, X509KeyUsageFlags enumeration [Security], XCN_CERT_CRL_SIGN_KEY_USAGE, XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE, XCN_CERT_DECIPHER_ONLY_KEY_USAGE, XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE, XCN_CERT_ENCIPHER_ONLY_KEY_USAGE, XCN_CERT_KEY_AGREEMENT_KEY_USAGE, XCN_CERT_KEY_CERT_SIGN_KEY_USAGE, XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE, XCN_CERT_NON_REPUDIATION_KEY_USAGE, XCN_CERT_NO_KEY_USAGE, XCN_CERT_OFFLINE_CRL_SIGN_KEY_USAGE, certenroll/X509KeyUsageFlags, certenroll/XCN_CERT_CRL_SIGN_KEY_USAGE, certenroll/XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE, certenroll/XCN_CERT_DECIPHER_ONLY_KEY_USAGE, certenroll/XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE, certenroll/XCN_CERT_ENCIPHER_ONLY_KEY_USAGE, certenroll/XCN_CERT_KEY_AGREEMENT_KEY_USAGE, certenroll/XCN_CERT_KEY_CERT_SIGN_KEY_USAGE, certenroll/XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE, certenroll/XCN_CERT_NON_REPUDIATION_KEY_USAGE, certenroll/XCN_CERT_NO_KEY_USAGE, certenroll/XCN_CERT_OFFLINE_CRL_SIGN_KEY_USAGE, security.x509keyusageflags_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509KeyUsageFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X509KeyUsageFlags
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509KeyUsageFlags enumeration


## -description


The <b>X509KeyUsageFlags</b> enumeration type specifies the purpose of a key contained in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>. You can use the enumeration to identify restrictions. For example, if a key should be used only for signing, you can select the <b>XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE</b> or the <b>XCN_CERT_NON_REPUDIATION_KEY_USAGE</b> values. Likewise, if a key should be used only for key management, you can select the <b>XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE</b> value. This enumeration can be used to initialize an <a href="https://msdn.microsoft.com/4325e6aa-99bb-4c9a-9b19-c5352ebf27b9">IX509ExtensionKeyUsage</a> object.


## -enum-fields




### -field XCN_CERT_NO_KEY_USAGE

The purpose of the key is not defined.


### -field XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE

The key is used with a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA) to support services other than nonrepudiation, certificate signing, or revocation list signing.


### -field XCN_CERT_NON_REPUDIATION_KEY_USAGE

The key is used to verify a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">digital signature</a> as part of a nonrepudiation service that protects against false denial of action by a signing entity.


### -field XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE

The key is used for key transport. That is, the key is used to manage a key passed from its point of origination to another point of use.


### -field XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE

The key is used to encrypt user data other than cryptographic keys.


### -field XCN_CERT_KEY_AGREEMENT_KEY_USAGE

The key is used for key agreement. The key agreement or key exchange protocol enables two or more parties to negotiate a key value without transferring the key and without previously establishing a shared secret.


### -field XCN_CERT_KEY_CERT_SIGN_KEY_USAGE

The key is used to verify a certificate signature. This value can only be used for certificates issued by <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authorities</a>.


### -field XCN_CERT_OFFLINE_CRL_SIGN_KEY_USAGE

The key is used to verify an offline <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) signature.


### -field XCN_CERT_CRL_SIGN_KEY_USAGE

The key is used to verify a CRL signature.


### -field XCN_CERT_ENCIPHER_ONLY_KEY_USAGE

The key is used to encrypt data while performing key agreement. When this value is specified, the <b>XCN_CERT_KEY_AGREEMENT_KEY_USAGE</b> value must also be specified.


### -field XCN_CERT_DECIPHER_ONLY_KEY_USAGE

The key is used to decrypt data while performing key agreement. When this value is specified, the <b>XCN_CERT_KEY_AGREEMENT_KEY_USAGE</b> must also be specified.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/4325e6aa-99bb-4c9a-9b19-c5352ebf27b9">IX509ExtensionKeyUsage</a>



<a href="https://msdn.microsoft.com/a4496125-862c-4ef0-93f3-a513eedeacd1">InitializeEncode</a>
 

 

