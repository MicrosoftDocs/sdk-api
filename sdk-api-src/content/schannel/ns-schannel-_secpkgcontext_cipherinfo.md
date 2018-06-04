---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SecPkgContext_CipherInfo structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Cipher info structure. This is returned by SECPKG_ATTR_CIPHER_INFO ulAttribute from the <a href="https://msdn.microsoft.com/0329e525-a743-4e6c-aac4-9f74274dadd2">QueryContextAttributes</a> (Schannel) function.


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

