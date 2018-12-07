---
UID: NF:certenroll.IX509PublicKey.InitializeFromEncodedPublicKeyInfo
title: IX509PublicKey::InitializeFromEncodedPublicKeyInfo
author: windows-sdk-content
description: Initializes the object from a byte array that contains a public key.
old-location: security\ix509publickey_initializefromencodedpublickeyinfo_method.htm
tech.root: seccertenroll
ms.assetid: 3e92d934-1ab7-4f09-a579-0dde4ef44c7f
ms.author: windowssdkdev
ms.date: 12/5/2018
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

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the key contained in the <i>strEncodedPublicKeyInfo</i> parameter. The default value is XCN_CRYPT_STRING_BASE64.


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



The <b>InitializeFromEncodedPublicKeyInfo</b> method initializes the following property values from an existing public key:

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
 

 

