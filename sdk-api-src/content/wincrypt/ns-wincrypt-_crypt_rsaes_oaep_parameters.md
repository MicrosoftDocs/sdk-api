---
UID: NS:wincrypt._CRYPT_RSAES_OAEP_PARAMETERS
title: "_CRYPT_RSAES_OAEP_PARAMETERS"
author: windows-sdk-content
description: Contains the parameters for an RSAES-OAEP key encryption.
old-location: security\crypt_rsaes_oaep_parameters.htm
old-project: SecCrypto
ms.assetid: ebcd25a2-2547-4949-85fd-be5f6c5bfcd2
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCRYPT_RSAES_OAEP_PARAMETERS, CRYPT_RSAES_OAEP_PARAMETERS, CRYPT_RSAES_OAEP_PARAMETERS structure [Security], PCRYPT_RSAES_OAEP_PARAMETERS, PCRYPT_RSAES_OAEP_PARAMETERS structure pointer [Security], _CRYPT_RSAES_OAEP_PARAMETERS, security.crypt_rsaes_oaep_parameters, wincrypt/CRYPT_RSAES_OAEP_PARAMETERS, wincrypt/PCRYPT_RSAES_OAEP_PARAMETERS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
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
tech.root: 
req.typenames: CRYPT_RSAES_OAEP_PARAMETERS, *PCRYPT_RSAES_OAEP_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_RSAES_OAEP_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_RSAES_OAEP_PARAMETERS structure


## -description


The <b>CRYPT_RSAES_OAEP_PARAMETERS</b> structure contains the parameters for an RSAES-OAEP key encryption. This structure is used with the <b>PKCS_RSAES_OAEP_PARAMETERS</b> and <b>szOID_RSAES_OAEP</b> encoding types.


## -struct-fields




### -field HashAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that identifies the hash algorithm to use. If this is not set for encoding, the default algorithm is <b>szOID_OIWSEC_sha1</b>.


### -field MaskGenAlgorithm

A <a href="https://msdn.microsoft.com/26ccf26d-9cde-4653-b4ab-7362f4fad640">CRYPT_MASK_GEN_ALGORITHM</a> structure that identifies the mask generation function to use. If this is not set for encoding, the default algorithm is <b>szOID_RSA_MGF1</b> with the mask generation hash algorithm defaulting to the algorithm specified by the <b>HashAlgorithm</b> member.


### -field PSourceAlgorithm

A <a href="https://msdn.microsoft.com/cd390487-2bba-4d57-a779-579ffbd16acb">CRYPT_PSOURCE_ALGORITHM</a> structure that contains the source of, and possibly the value of, the label to be used. If this is not set for encoding, the default algorithm is <b>szOID_RSA_PSPECIFIED</b> with no OCTET bytes.


## -remarks



RSAES-OAEP is normally used for encrypting AES symmetric keys. Normally, only the hash algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) will need to be set for encoding. For decoding, all the members are explicitly set.



