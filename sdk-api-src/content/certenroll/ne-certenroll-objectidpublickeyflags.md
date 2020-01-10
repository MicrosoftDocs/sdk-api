---
UID: NE:certenroll.ObjectIdPublicKeyFlags
title: ObjectIdPublicKeyFlags (certenroll.h)
description: Specifies whether a public key algorithm is used for signing or for encryption.
old-location: security\objectidpublickeyflags_enum.htm
tech.root: seccertenroll
ms.assetid: f41a871a-0247-4c49-b6a0-66d31c54a0e3
ms.date: 12/05/2018
ms.keywords: ObjectIdPublicKeyFlags, ObjectIdPublicKeyFlags enumeration [Security], XCN_CRYPT_OID_INFO_PUBKEY_ANY, XCN_CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG, XCN_CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG, certenroll/ObjectIdPublicKeyFlags, certenroll/XCN_CRYPT_OID_INFO_PUBKEY_ANY, certenroll/XCN_CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG, certenroll/XCN_CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG, security.objectidpublickeyflags_enum
f1_keywords:
- certenroll/ObjectIdPublicKeyFlags
dev_langs:
- c++
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
- ObjectIdPublicKeyFlags
targetos: Windows
req.typenames: ObjectIdPublicKeyFlags
req.redist: 
ms.custom: 19H1
---

# ObjectIdPublicKeyFlags enumeration


## -description


The <b>ObjectIdPublicKeyFlags</b> enumeration type specifies whether a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">public key</a> algorithm is used for signing or for <a href="https://docs.microsoft.com/windows/desktop/SecGloss/e-gly">encryption</a>. Some algorithms, such as <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">RSA</a>, can be used for both purposes. This enumeration is used by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromalgorithmname">InitializeFromAlgorithmName</a> method on the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface to narrow and disambiguate the algorithm search.


## -enum-fields




### -field XCN_CRYPT_OID_INFO_PUBKEY_ANY

The algorithm can be used for signing or encryption.


### -field XCN_CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG

The algorithm is used for signing.


### -field XCN_CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG

The algorithm is used for encryption.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromalgorithmname">InitializeFromAlgorithmName</a>
 

 

