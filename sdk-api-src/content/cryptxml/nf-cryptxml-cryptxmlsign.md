---
UID: NF:cryptxml.CryptXmlSign
title: CryptXmlSign function
author: windows-sdk-content
description: Creates a cryptographic signature of a SignedInfo element.
old-location: security\cryptxmlsign.htm
tech.root: seccrypto
ms.assetid: 38bd365e-bc63-498c-a650-471429f09d37
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: AT_KEYEXCHANGE, AT_SIGNATURE, CERT_NCRYPT_KEY_SPEC, CRYPT_XML_FLAG_DISABLE_EXTENSIONS, CRYPT_XML_SIGN_ADD_KEYVALUE, CryptXmlSign, CryptXmlSign function [Security], cryptxml/CryptXmlSign, security.cryptxmlsign
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: cryptxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptxml.dll
api_name:
 - CryptXmlSign
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlSign function


## -description


The <b>CryptXmlSign</b> function creates a cryptographic signature of  a <b>SignedInfo</b> element.


## -parameters




### -param hSignature [in]

The handle to a <a href="https://msdn.microsoft.com/en-us/library/Dd433864(v=VS.85).aspx">CRYPT_XML_SIGNATURE</a> structure. 


### -param hKey [in, optional]

The handle of a <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> used to sign the <b>SignedInfo</b> element.
    This parameter must be <b>NULL</b> for HMAC-based signature algorithms.


### -param dwKeySpec

A <b>DWORD</b> value that specifies the key type. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/en-us/library/ms721590(v=VS.85).aspx">key pair</a> is a key exchange pair.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The key pair is a signature pair.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NCRYPT_KEY_SPEC"></a><a id="cert_ncrypt_key_spec"></a><dl>
<dt><b>CERT_NCRYPT_KEY_SPEC</b></dt>
<dt>0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
The key is a Cryptography API: Next Generation (CNG) key.

</td>
</tr>
</table>
 


### -param dwFlags

A <b>DWORD</b> value that controls how the data is signed. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_SIGN_ADD_KEYVALUE"></a><a id="crypt_xml_sign_add_keyvalue"></a><dl>
<dt><b>CRYPT_XML_SIGN_ADD_KEYVALUE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Populate the <b>KeyValue</b> element from  the handle specified in the <i>hKey</i> parameter.


<div class="alert"><b>Important</b>  The <b>CRYPT_XML_SIGN_ADD_KEYVALUE</b> flag cannot be used when the <i>dwKeyInfoSpec</i> parameter is set to <b>CRYPT_XML_KEYINFO_SPEC_ENCODED</b>.</div>
<div> </div>


</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_FLAG_DISABLE_EXTENSIONS"></a><a id="crypt_xml_flag_disable_extensions"></a><dl>
<dt><b>CRYPT_XML_FLAG_DISABLE_EXTENSIONS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Only default implementations for the signature and
digest  are used.  When this flag is set, no other registered extensions are loaded.

</td>
</tr>
</table>
 


### -param dwKeyInfoSpec

The type of data structure pointed to by the <i>pvKeyInfoSpec</i> parameter. Here are some possible combinations.

<table>
<tr>
<th><i>dwKeyInfec</i></th>
<th><i>pvKeyInfoSpec</i></th>
</tr>
<tr>
<td>
<b>CRYPT_XML_KEYINFO_SPEC_NONE</b>

</td>
<td>
Is set to  <b>NULL</b>

</td>
</tr>
<tr>
<td>
<b>CRYPT_XML_KEYINFO_SPEC_ENCODED</b>

</td>
<td>
Points to a <a href="https://msdn.microsoft.com/en-us/library/Dd433844(v=VS.85).aspx">CRYPT_XML_BLOB</a> structure

</td>
</tr>
<tr>
<td>
<b>CRYPT_XML_KEYINFO_SPEC_PARAM</b>

</td>
<td>
Points to a <a href="https://msdn.microsoft.com/en-us/library/Dd433851(v=VS.85).aspx">CRYPT_XML_KEYINFO_PARAM</a> structure

</td>
</tr>
</table>
 


### -param pvKeyInfoSpec [in, optional]

A pointer to a structure, the type of which is determined by the value of the <i>dwKeyInfoSpec</i> parameter.


### -param pSignatureMethod [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd433842(v=VS.85).aspx">CRYPT_XML_ALGORITHM</a>     structure that specifies the signature method.


### -param pCanonicalization [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd433842(v=VS.85).aspx">CRYPT_XML_ALGORITHM</a>     structure that specifies the canonicalization method.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



