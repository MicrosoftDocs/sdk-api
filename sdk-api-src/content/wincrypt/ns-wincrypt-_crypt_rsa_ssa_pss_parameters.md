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

