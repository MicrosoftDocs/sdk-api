---
UID: NE:certenroll.ObjectIdPublicKeyFlags
title: ObjectIdPublicKeyFlags
author: windows-sdk-content
description: Specifies whether a public key algorithm is used for signing or for encryption.
old-location: security\objectidpublickeyflags_enum.htm
old-project: seccertenroll
ms.assetid: f41a871a-0247-4c49-b6a0-66d31c54a0e3
ms.author: windowssdkdev
ms.date: 07/30/2018
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


The <b>ObjectIdPublicKeyFlags</b> enumeration type specifies whether a <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key</a> algorithm is used for signing or for <a href="https://msdn.microsoft.com/en-us/library/ms721575(v=VS.85).aspx">encryption</a>. Some algorithms, such as <a href="https://msdn.microsoft.com/en-us/library/ms721604(v=VS.85).aspx">RSA</a>, can be used for both purposes. This enumeration is used by the <a href="https://msdn.microsoft.com/en-us/library/Aa376796(v=VS.85).aspx">InitializeFromAlgorithmName</a> method on the <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> interface to narrow and disambiguate the algorithm search.


## -enum-fields




### -field XCN_CRYPT_OID_INFO_PUBKEY_ANY

The algorithm can be used for signing or encryption.


### -field XCN_CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG

The algorithm is used for signing.


### -field XCN_CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG

The algorithm is used for encryption.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376796(v=VS.85).aspx">InitializeFromAlgorithmName</a>
 

 

