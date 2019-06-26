---
UID: NS:schannel._SecPkgContext_CipherInfo
title: SecPkgContext_CipherInfo (schannel.h)
author: windows-sdk-content
description: Cipher info structure. This is returned by SECPKG_ATTR_CIPHER_INFO ulAttribute from the QueryContextAttributes (Schannel) function.
old-location: security\secpkgcontext_cipherinfo.htm
tech.root: SecAuthN
ms.assetid: 204D3520-76B6-42C0-83A4-45769F66364A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSecPkgContext_CipherInfo, PSecPkgContext_CipherInfo, PSecPkgContext_CipherInfo structure pointer [Security], SecPkgContext_CipherInfo, SecPkgContext_CipherInfo structure [Security], schannel/PSecPkgContext_CipherInfo, schannel/SecPkgContext_CipherInfo, security.secpkgcontext_cipherinfo"
ms.topic: struct
f1_keywords: 
 - "schannel/SecPkgContext_CipherInfo"
req.header: schannel.h
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
 - Schannel.h
api_name:
 - SecPkgContext_CipherInfo
product: Windows
targetos: Windows
req.typenames: SecPkgContext_CipherInfo, *PSecPkgContext_CipherInfo
req.redist: 
ms.custom: 19H1
---

# SecPkgContext_CipherInfo structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Cipher info structure. This is returned by SECPKG_ATTR_CIPHER_INFO ulAttribute from the <a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querycontextattributesw">QueryContextAttributes</a> (Schannel) function.


## -struct-fields




### -field dwVersion

The dw version.


### -field dwProtocol

The dw protocol.


### -field dwCipherSuite

The dw cipher suite.


### -field dwBaseCipherSuite

The dw base cipher suite.


### -field szCipherSuite

 


### -field szCipher

 


### -field dwCipherLen

The dw cipher length.


### -field dwCipherBlockLen

The dw cipher block length in bytes.


### -field szHash

 


### -field dwHashLen

The dw hash length.


### -field szExchange

 


### -field dwMinExchangeLen

The dw min exchange length.


### -field dwMaxExchangeLen

The dw max exchange length.


### -field szCertificate

 


### -field dwKeyType

The dw key type.


#### - szCertificate[SZ_ALG_MAX_SIZE]

The sz certificate.


#### - szCipherSuite[SZ_ALG_MAX_SIZE]

The sz cipher suite.


#### - szCipher[SZ_ALG_MAX_SIZE]

The sz cipher.


#### - szExchange[SZ_ALG_MAX_SIZE]

The sz exchange.


#### - szHash[SZ_ALG_MAX_SIZE]

The sz hash.

