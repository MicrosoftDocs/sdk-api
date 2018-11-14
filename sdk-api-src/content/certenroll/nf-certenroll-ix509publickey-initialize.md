---
UID: NF:certenroll.IX509PublicKey.Initialize
title: IX509PublicKey::Initialize
author: windows-sdk-content
description: Initializes the object from a public key algorithm object identifier (OID) and from byte arrays that contain a public key and the associated parameters, if any.
old-location: security\ix509publickey_initialize_method.htm
tech.root: SecCertEnroll
ms.assetid: b6db46b2-95f5-4ba9-829d-97bf83fd9806
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509PublicKey interface [Security],Initialize method, IX509PublicKey.Initialize, IX509PublicKey::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509PublicKey interface, certenroll/IX509PublicKey::Initialize, security.ix509publickey_initialize_method
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
 - IX509PublicKey.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509PublicKey.Initialize
: 
---

# IX509PublicKey::Initialize


## -description


The <b>Initialize</b> method initializes the object from a public key  algorithm <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) and from byte arrays that contain a public key and the associated parameters, if any. The byte arrays are represented by Unicode-encoded strings.


## -parameters




### -param pObjectId [in]

Pointer to an  <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> interface that represents the algorithm OID.


### -param strEncodedKey [in]

A <b>BSTR</b> variable that contains the public key.


### -param strEncodedParameters [in]

A <b>BSTR</b> variable that contains the parameters associated with the public key. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa379043(v=VS.85).aspx">EncodedParameters</a> property.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode-encoding applied to the  arguments specified in the <i>strEncodedKey</i> and <i>strEncodedParameters</i> parameters. The default value is XCN_CRYPT_STRING_BASE64.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

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
<a href="https://msdn.microsoft.com/en-us/library/Aa379040(v=VS.85).aspx">Algorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379042(v=VS.85).aspx">EncodedKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379043(v=VS.85).aspx">EncodedParameters</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379046(v=VS.85).aspx">Length</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa379039(v=VS.85).aspx">IX509PublicKey</a>
 

 

