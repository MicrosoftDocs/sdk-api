---
UID: NS:wincrypt._CRYPT_RSA_SSA_PSS_PARAMETERS
title: "_CRYPT_RSA_SSA_PSS_PARAMETERS"
author: windows-driver-content
description: Contains the parameters for an RSA PKCS #1 v2.1 signature.
old-location: security\crypt_rsa_ssa_pss_parameters.htm
old-project: SecCrypto
ms.assetid: 3887e6c7-17df-42d3-82b1-a8f410321ba0
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: "*PCRYPT_RSA_SSA_PSS_PARAMETERS, CRYPT_RSA_SSA_PSS_PARAMETERS, CRYPT_RSA_SSA_PSS_PARAMETERS structure [Security], PCRYPT_RSA_SSA_PSS_PARAMETERS, PCRYPT_RSA_SSA_PSS_PARAMETERS structure pointer [Security], _CRYPT_RSA_SSA_PSS_PARAMETERS, security.crypt_rsa_ssa_pss_parameters, wincrypt/CRYPT_RSA_SSA_PSS_PARAMETERS, wincrypt/PCRYPT_RSA_SSA_PSS_PARAMETERS"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CRYPT_RSA_SSA_PSS_PARAMETERS, *PCRYPT_RSA_SSA_PSS_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CRYPT_RSA_SSA_PSS_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_RSA_SSA_PSS_PARAMETERS structure


## -description


The <b>CRYPT_RSA_SSA_PSS_PARAMETERS</b> structure contains the parameters for an RSA PKCS #1 v2.1 signature. This structure is used with the <b>PKCS_RSA_SSA_PSS_PARAMETERS</b> and <b>szOID_RSA_SSA_PSS</b> encoding types.


## -struct-fields




### -field HashAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that identifies the hash algorithm to use. If this is not set for encoding, the default algorithm is <b>szOID_OIWSEC_sha1</b>.


### -field MaskGenAlgorithm

A <a href="https://msdn.microsoft.com/26ccf26d-9cde-4653-b4ab-7362f4fad640">CRYPT_MASK_GEN_ALGORITHM</a> structure that identifies the mask generation function to use. If this is not set for encoding, the default algorithm is <b>szOID_RSA_MGF1</b> with the mask generation hash algorithm defaulting to the hash algorithm.


### -field dwSaltLength

The octet length of the salt. If this is not set for encoding, the default salt length is the length of the hash value.


### -field dwTrailerField

The trailer field number. If this is not set for encoding, the default is <b>PKCS_RSA_SSA_PSS_TRAILER_FIELD_BC</b>.

