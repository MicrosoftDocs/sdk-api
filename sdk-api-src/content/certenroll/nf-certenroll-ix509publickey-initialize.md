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

# IX509PublicKey::Initialize


## -description


The <b>Initialize</b> method initializes the object from a public key  algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and from byte arrays that contain a public key and the associated parameters, if any. The byte arrays are represented by Unicode-encoded strings.


## -parameters




### -param pObjectId [in]

Pointer to an  <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface that represents the algorithm OID.


### -param strEncodedKey [in]

A <b>BSTR</b> variable that contains the public key.


### -param strEncodedParameters [in]

A <b>BSTR</b> variable that contains the parameters associated with the public key. For more information, see the <a href="https://msdn.microsoft.com/f7c7bf0a-0b66-4676-9448-f74937823f90">EncodedParameters</a> property.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode-encoding applied to the  arguments specified in the <i>strEncodedKey</i> and <i>strEncodedParameters</i> parameters. The default value is XCN_CRYPT_STRING_BASE64.


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



The <b>Initialize</b> method initializes the following property values:

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
 

 

