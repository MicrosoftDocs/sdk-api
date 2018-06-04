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

# BCryptEnumAlgorithms function


## -description


The <b>BCryptEnumAlgorithms</b> function gets a list of the registered algorithm identifiers.


## -parameters




### -param dwAlgOperations [in]

A value that specifies the algorithm operation types to include in the enumeration. This can be a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_CIPHER_OPERATION"></a><a id="bcrypt_cipher_operation"></a><dl>
<dt><b>BCRYPT_CIPHER_OPERATION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Include the cipher algorithms in the enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_OPERATION"></a><a id="bcrypt_hash_operation"></a><dl>
<dt><b>BCRYPT_HASH_OPERATION</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Include the hash algorithms in the enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION"></a><a id="bcrypt_asymmetric_encryption_operation"></a><dl>
<dt><b>BCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Include the asymmetric encryption algorithms in the enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SECRET_AGREEMENT_OPERATION"></a><a id="bcrypt_secret_agreement_operation"></a><dl>
<dt><b>BCRYPT_SECRET_AGREEMENT_OPERATION</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Include the secret agreement algorithms in the enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SIGNATURE_OPERATION"></a><a id="bcrypt_signature_operation"></a><dl>
<dt><b>BCRYPT_SIGNATURE_OPERATION</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Include the signature algorithms in the enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RNG_OPERATION"></a><a id="bcrypt_rng_operation"></a><dl>
<dt><b>BCRYPT_RNG_OPERATION</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Include the random number generator (RNG) algorithms in the enumeration.

</td>
</tr>
</table>
 


### -param pAlgCount [out]

A pointer to a <b>ULONG</b> variable to receive the number of elements in the <i>ppAlgList</i> array.


### -param ppAlgList [out]

The address of a <a href="https://msdn.microsoft.com/a49a21c9-5668-4709-b52a-f6cacd944845">BCRYPT_ALGORITHM_IDENTIFIER</a> structure pointer to receive the array of registered algorithm identifiers. This pointer must be passed to the <a href="https://msdn.microsoft.com/0ee83ca1-2fe6-4ff2-823e-888b3e66f310">BCryptFreeBuffer</a> function when it is no longer needed.


### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are defined for this function.


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -remarks




<b>BCryptEnumAlgorithms</b> can be called either from user mode or kernel mode. Kernel mode callers must be executing at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/library/windows/hardware/ff551779">IRQL</a>.



