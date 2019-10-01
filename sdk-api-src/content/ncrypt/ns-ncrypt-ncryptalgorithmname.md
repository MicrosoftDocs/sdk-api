---
UID: NS:ncrypt._NCryptAlgorithmName
title: NCryptAlgorithmName (ncrypt.h)
author: windows-sdk-content
description: Used to contain information about a CNG algorithm.
old-location: security\ncryptalgorithmname_struct.htm
tech.root: SecCNG
ms.assetid: 79b0193e-3be8-46ce-a422-40ed9698363f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, NCRYPT_SECRET_AGREEMENT_INTERFACE, NCRYPT_SECRET_AGREEMENT_OPERATION, NCRYPT_SIGNATURE_INTERFACE, NCRYPT_SIGNATURE_OPERATION, NCryptAlgorithmName, NCryptAlgorithmName structure [Security], ncrypt/NCryptAlgorithmName, security.ncryptalgorithmname_struct
ms.topic: struct
f1_keywords: 
 - "ncrypt/NCryptAlgorithmName"
req.header: ncrypt.h
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
 - Ncrypt.h
api_name:
 - NCryptAlgorithmName
targetos: Windows
req.typenames: NCryptAlgorithmName
req.redist: 
ms.custom: 19H1
---

# NCryptAlgorithmName structure


## -description


The <b>NCryptAlgorithmName</b> structure is used to contain information about a CNG algorithm.


## -struct-fields




### -field pszName

A pointer to a null-terminated Unicode string that contains the name of the algorithm. This can be one of the standard <a href="https://docs.microsoft.com/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a> or the identifier for another registered algorithm.


### -field dwClass

A <b>DWORD</b> value that defines which algorithm class this algorithm belongs to. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></a><a id="ncrypt_asymmetric_encryption_interface"></a><dl>
<dt><b>NCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The algorithm belongs to the asymmetric encryption class of algorithms.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SECRET_AGREEMENT_INTERFACE"></a><a id="ncrypt_secret_agreement_interface"></a><dl>
<dt><b>NCRYPT_SECRET_AGREEMENT_INTERFACE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The algorithm belongs to the secret agreement (Diffie-Hellman) class of algorithms.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SIGNATURE_INTERFACE"></a><a id="ncrypt_signature_interface"></a><dl>
<dt><b>NCRYPT_SIGNATURE_INTERFACE</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
The algorithm belongs to the signature class of algorithms.

</td>
</tr>
</table>
 


### -field dwAlgOperations

A <b>DWORD</b> value that defines which operational classes this algorithm belongs to. This can be a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION"></a><a id="ncrypt_asymmetric_encryption_operation"></a><dl>
<dt><b>NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The algorithm is an asymmetric encryption algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SECRET_AGREEMENT_OPERATION"></a><a id="ncrypt_secret_agreement_operation"></a><dl>
<dt><b>NCRYPT_SECRET_AGREEMENT_OPERATION</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The algorithm is a secret agreement (Diffie-Hellman) algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SIGNATURE_OPERATION"></a><a id="ncrypt_signature_operation"></a><dl>
<dt><b>NCRYPT_SIGNATURE_OPERATION</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The algorithm is a digital signature algorithm.

</td>
</tr>
</table>
 


### -field dwFlags

A set of flags that provide more information about the algorithm.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ncrypt/nf-ncrypt-ncryptenumalgorithms">NCryptEnumAlgorithms</a>
 

 

