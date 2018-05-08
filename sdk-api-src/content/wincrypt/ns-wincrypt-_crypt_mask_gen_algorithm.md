---
UID: NS:wincrypt._CRYPT_MASK_GEN_ALGORITHM
title: "_CRYPT_MASK_GEN_ALGORITHM"
author: windows-driver-content
description: Identifies the algorithm used to generate an RSA PKCS #1 v2.1 signature mask.
old-location: security\crypt_mask_gen_algorithm.htm
old-project: SecCrypto
ms.assetid: 26ccf26d-9cde-4653-b4ab-7362f4fad640
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: "*PCRYPT_MASK_GEN_ALGORITHM, CRYPT_MASK_GEN_ALGORITHM, CRYPT_MASK_GEN_ALGORITHM structure [Security], PCRYPT_MASK_GEN_ALGORITHM, PCRYPT_MASK_GEN_ALGORITHM structure pointer [Security], _CRYPT_MASK_GEN_ALGORITHM, security.crypt_mask_gen_algorithm, szOID_RSA_MGF1, wincrypt/CRYPT_MASK_GEN_ALGORITHM, wincrypt/PCRYPT_MASK_GEN_ALGORITHM"
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
req.typenames: CRYPT_MASK_GEN_ALGORITHM, *PCRYPT_MASK_GEN_ALGORITHM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CRYPT_MASK_GEN_ALGORITHM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_MASK_GEN_ALGORITHM structure


## -description


The <b>CRYPT_MASK_GEN_ALGORITHM</b> structure identifies the algorithm used to generate an RSA PKCS #1 v2.1 signature mask.


## -struct-fields




### -field pszObjId

The address of a null-terminated ANSI string that contains the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the mask generation algorithm. This can be the following value or any other mask generation function OID.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="szOID_RSA_MGF1"></a><a id="szoid_rsa_mgf1"></a><a id="SZOID_RSA_MGF1"></a><dl>
<dt><b>szOID_RSA_MGF1</b></dt>
<dt>"1.2.840.113549.1.1.8"</dt>
</dl>
</td>
<td width="60%">
The RSA MGF1 function.

</td>
</tr>
</table>
 


### -field HashAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that identifies the hash algorithm to use for the mask generation.


## -see-also




<a href="https://msdn.microsoft.com/ebcd25a2-2547-4949-85fd-be5f6c5bfcd2">CRYPT_RSAES_OAEP_PARAMETERS</a>



<a href="https://msdn.microsoft.com/3887e6c7-17df-42d3-82b1-a8f410321ba0">CRYPT_RSA_SSA_PSS_PARAMETERS</a>
 

 

