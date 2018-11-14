---
UID: NF:certenroll.IX509PrivateKey.Import
title: IX509PrivateKey::Import
author: windows-sdk-content
description: Imports an existing private key into a key container within a cryptographic provider.
old-location: security\ix509privatekey_import_method.htm
tech.root: SecCertEnroll
ms.assetid: 33e335e2-9c3f-4aa1-a393-db0ee8095b64
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BCRYPT_PRIVATE_KEY_BLOB, IX509PrivateKey interface [Security],Import method, IX509PrivateKey.Import, IX509PrivateKey::Import, Import, Import method [Security], Import method [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::Import, security.ix509privatekey_import_method
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
 - IX509PrivateKey.Import
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
- IX509PrivateKey.Import
: 
---

# IX509PrivateKey::Import


## -description


The <b>Import</b> method imports an existing private key into a key container within a cryptographic provider.


## -parameters




### -param strExportType [in]

If the key was created by using a CNG KSP (Key Storage Provider), the <b>Import</b> method passes this argument to the <i>pszProperty</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/Aa376292(v=VS.85).aspx">NCryptSetProperty</a> function. That is, the value you specify will be used as the name of a property to be set on the imported key.

If the key was created by using a CryptoAPI CSP (Cryptographic Service Provider), this argument specifies how the private key is to be imported. This can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PRIVATE_KEY_BLOB"></a><a id="bcrypt_private_key_blob"></a><dl>
<dt><b>BCRYPT_PRIVATE_KEY_BLOB</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Imports the entire private key.

</td>
</tr>
</table>
 


### -param strEncodedKey [in]

A <b>BSTR</b> variable that contains the key to import.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding to be applied to the string contained in the <i>strEncodedKey</i> parameter. The default value is XCN_CRYPT_STRING_BASE64.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_READ_ONLY)</b></dt>
</dl>
</td>
<td width="60%">
The key container is already open. You can receive this error if you have already called <a href="https://msdn.microsoft.com/en-us/library/Aa379027(v=VS.85).aspx">Open</a> or <a href="https://msdn.microsoft.com/en-us/library/Aa378957(v=VS.85).aspx">Create</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_CALL_NOT_IMPLEMENTED)</b></dt>
</dl>
</td>
<td width="60%">
The key was created by a CryptoAPI CSP and you specified a value other than BCRYPT_PRIVATE_KEY_BLOB for the <i>strExportType</i> parameter.

</td>
</tr>
</table>
 




## -remarks



The <b>Import</b> function automatically assumes that you are attempting to import a CNG KSP key if you specify a value other than BCRYPT_PRIVATE_KEY_BLOB for the <i>strExportType</i> parameter and you do not set any of the following properties:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378972(v=VS.85).aspx">CspStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379022(v=VS.85).aspx">LegacyCsp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379031(v=VS.85).aspx">ProviderName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379032(v=VS.85).aspx">ProviderType</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
 

 

