---
UID: NF:certenroll.IX509PublicKey.ComputeKeyIdentifier
title: IX509PublicKey::ComputeKeyIdentifier
author: windows-sdk-content
description: Creates an identifier from a 160-bit SHA-1 hash of the public key.
old-location: security\ix509publickey_computekeyidentifier_method.htm
tech.root: seccertenroll
ms.assetid: b2e471c7-1087-46a2-8938-5d3cea44f7f7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ComputeKeyIdentifier, ComputeKeyIdentifier method [Security], ComputeKeyIdentifier method [Security],IX509PublicKey interface, IX509PublicKey interface [Security],ComputeKeyIdentifier method, IX509PublicKey.ComputeKeyIdentifier, IX509PublicKey::ComputeKeyIdentifier, certenroll/IX509PublicKey::ComputeKeyIdentifier, security.ix509publickey_computekeyidentifier_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
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
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PublicKey.ComputeKeyIdentifier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PublicKey::ComputeKeyIdentifier


## -description


The <b>ComputeKeyIdentifier</b> method creates an identifier from a 160-bit SHA-1 hash of the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>.


## -parameters




### -param Algorithm [in]

A value of the <a href="https://msdn.microsoft.com/80e3c730-880f-4cfa-921f-3bb88cf827f2">KeyIdentifierHashAlgorithm</a> enumeration that specifies what hash algorithm to use to create the key identifier.

If this value is SKIHashDefault or SKIHashSha1, the identifier is created by hashing only the byte array that contains the key and excluding the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) tag, length, and unused bits fields.

If this value is SKIHashCapiSha1, the identifier is created by hashing the DER-encoded byte array that contains the tag, length,  number of unused bits, and the public key.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode-encoding to be applied to the hash contained in the <i>pValue</i> parameter. The default value is XCN_CRYPT_STRING_BASE64.


### -param pValue [out]

Pointer to a <b>BSTR</b> variable that contains the key identifier.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CERTSRV_E_PROPERTY_EMPTY</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The algorithm object identifier or the public key parameters could not be found.

</td>
</tr>
</table>
 




## -remarks



You must call the <a href="https://msdn.microsoft.com/3e92d934-1ab7-4f09-a579-0dde4ef44c7f">InitializeFromEncodedPublicKeyInfo</a> method or the <a href="https://msdn.microsoft.com/b6db46b2-95f5-4ba9-829d-97bf83fd9806">Initialize</a> method to initialize the public key object before calling  <b>ComputeKeyIdentifier</b>.




## -see-also




<a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a>
 

 

