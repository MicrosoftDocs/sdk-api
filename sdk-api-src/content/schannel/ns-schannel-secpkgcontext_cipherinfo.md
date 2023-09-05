---
UID: NS:schannel._SecPkgContext_CipherInfo
title: SecPkgContext_CipherInfo (schannel.h)
description: Cipher info structure. This is returned by SECPKG_ATTR_CIPHER_INFO ulAttribute from the QueryContextAttributes (Schannel) function.
helpviewer_keywords: ["*PSecPkgContext_CipherInfo","PSecPkgContext_CipherInfo","PSecPkgContext_CipherInfo structure pointer [Security]","SecPkgContext_CipherInfo","SecPkgContext_CipherInfo structure [Security]","schannel/PSecPkgContext_CipherInfo","schannel/SecPkgContext_CipherInfo","security.secpkgcontext_cipherinfo"]
old-location: security\secpkgcontext_cipherinfo.htm
tech.root: security
ms.assetid: 204D3520-76B6-42C0-83A4-45769F66364A
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_CipherInfo, PSecPkgContext_CipherInfo, PSecPkgContext_CipherInfo structure pointer [Security], SecPkgContext_CipherInfo, SecPkgContext_CipherInfo structure [Security], schannel/PSecPkgContext_CipherInfo, schannel/SecPkgContext_CipherInfo, security.secpkgcontext_cipherinfo'
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
targetos: Windows
req.typenames: SecPkgContext_CipherInfo, *PSecPkgContext_CipherInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_CipherInfo
 - schannel/_SecPkgContext_CipherInfo
 - PSecPkgContext_CipherInfo
 - schannel/PSecPkgContext_CipherInfo
 - SecPkgContext_CipherInfo
 - schannel/SecPkgContext_CipherInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Schannel.h
api_name:
 - SecPkgContext_CipherInfo
---

## -description

Cipher info structure. This is returned by SECPKG_ATTR_CIPHER_INFO ulAttribute from the <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesw">QueryContextAttributes</a> (Schannel) function.

## -struct-fields

### -field dwVersion

The dw version.

### -field dwProtocol

The dw protocol.

### -field dwCipherSuite

The dw cipher suite.

### -field dwBaseCipherSuite

The dw base cipher suite.

### -field dwCipherLen

The dw cipher length.

### -field dwCipherBlockLen

The dw cipher block length in bytes.

### -field dwHashLen

The dw hash length.

### -field dwMinExchangeLen

The dw min exchange length.

### -field dwMaxExchangeLen

The dw max exchange length.

### -field dwKeyType

The dw key type.

### -field szCertificate

The sz certificate.

### -field szCipherSuite

The sz cipher suite.

### -field szCipher

The sz cipher.

### -field szExchange

The sz exchange.

### -field szHash

The sz hash.
