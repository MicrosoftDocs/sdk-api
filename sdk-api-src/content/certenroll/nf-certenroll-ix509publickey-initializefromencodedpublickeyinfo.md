---
UID: NF:certenroll.IX509PublicKey.InitializeFromEncodedPublicKeyInfo
title: IX509PublicKey::InitializeFromEncodedPublicKeyInfo
author: windows-sdk-content
description: Initializes the object from a byte array that contains a public key.
old-location: security\ix509publickey_initializefromencodedpublickeyinfo_method.htm
tech.root: seccertenroll
ms.assetid: 3e92d934-1ab7-4f09-a579-0dde4ef44c7f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IX509PublicKey interface [Security],InitializeFromEncodedPublicKeyInfo method, IX509PublicKey.InitializeFromEncodedPublicKeyInfo, IX509PublicKey::InitializeFromEncodedPublicKeyInfo, InitializeFromEncodedPublicKeyInfo, InitializeFromEncodedPublicKeyInfo method [Security], InitializeFromEncodedPublicKeyInfo method [Security],IX509PublicKey interface, certenroll/IX509PublicKey::InitializeFromEncodedPublicKeyInfo, security.ix509publickey_initializefromencodedpublickeyinfo_method
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
 - IX509PublicKey.InitializeFromEncodedPublicKeyInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PublicKey::InitializeFromEncodedPublicKeyInfo


## -description


The <b>InitializeFromEncodedPublicKeyInfo</b> method initializes the object from a byte array that contains a public key. The byte array is represented by a Unicode-encoded string.


## -parameters




### -param strEncodedPublicKeyInfo [in]

A <b>BSTR</b> variable that contains the key.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the key contained in the <i>strEncodedPublicKeyInfo</i> parameter. The default value is XCN_CRYPT_STRING_BASE64.


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
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>InitializeFromEncodedPublicKeyInfo</b> method initializes the following property values from an existing public key:

<ul>
<li>
<a href="https://msdn.microsoft.com/6c34323e-669e-434c-946f-65fe53456a11">Algorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3573f4b6-ecfd-4540-bc43-c88943992fe2">EncodedKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f7c7bf0a-0b66-4676-9448-f74937823f90">EncodedParameters</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c386fb27-84c5-4570-9cdb-202baa726b96">Length</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a>
 

 

