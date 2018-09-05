---
UID: NE:certenroll.ObjectIdPublicKeyFlags
title: ObjectIdPublicKeyFlags
author: windows-sdk-content
description: Specifies whether a public key algorithm is used for signing or for encryption.
old-location: security\objectidpublickeyflags_enum.htm
old-project: SecCertEnroll
ms.assetid: f41a871a-0247-4c49-b6a0-66d31c54a0e3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ObjectIdPublicKeyFlags, ObjectIdPublicKeyFlags enumeration [Security], XCN_CRYPT_OID_INFO_PUBKEY_ANY, XCN_CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG, XCN_CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG, certenroll/ObjectIdPublicKeyFlags, certenroll/XCN_CRYPT_OID_INFO_PUBKEY_ANY, certenroll/XCN_CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG, certenroll/XCN_CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG, security.objectidpublickeyflags_enum
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
req.typenames: ObjectIdPublicKeyFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - ObjectIdPublicKeyFlags
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ObjectIdPublicKeyFlags enumeration


## -description


The <b>ObjectIdPublicKeyFlags</b> enumeration type specifies whether a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> algorithm is used for signing or for <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">encryption</a>. Some algorithms, such as <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RSA</a>, can be used for both purposes. This enumeration is used by the <a href="https://msdn.microsoft.com/ba8c1f11-9380-43a9-b444-b0fff114a176">InitializeFromAlgorithmName</a> method on the <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface to narrow and disambiguate the algorithm search.


## -enum-fields




### -field XCN_CRYPT_OID_INFO_PUBKEY_ANY

The algorithm can be used for signing or encryption.


### -field XCN_CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG

The algorithm is used for signing.


### -field XCN_CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG

The algorithm is used for encryption.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/ba8c1f11-9380-43a9-b444-b0fff114a176">InitializeFromAlgorithmName</a>
 

 

