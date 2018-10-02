---
UID: NF:certenroll.IX509ExtensionKeyUsage.InitializeEncode
title: IX509ExtensionKeyUsage::InitializeEncode
author: windows-sdk-content
description: Initializes the extension by using the X509KeyUsageFlags enumeration.
old-location: security\ix509extensionkeyusage_initializeencode_method.htm
tech.root: SecCertEnroll
ms.assetid: a4496125-862c-4ef0-93f3-a513eedeacd1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509ExtensionKeyUsage interface [Security],InitializeEncode method, IX509ExtensionKeyUsage.InitializeEncode, IX509ExtensionKeyUsage::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509ExtensionKeyUsage interface, XCN_CERT_CRL_SIGN_KEY_USAGE, XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE, XCN_CERT_DECIPHER_ONLY_KEY_USAGE, XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE, XCN_CERT_ENCIPHER_ONLY_KEY_USAGE, XCN_CERT_KEY_AGREEMENT_KEY_USAGE, XCN_CERT_KEY_CERT_SIGN_KEY_USAGE, XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE, XCN_CERT_NON_REPUDIATION_KEY_USAGE, XCN_CERT_OFFLINE_CRL_SIGN_KEY_USAGE, certenroll/IX509ExtensionKeyUsage::InitializeEncode, security.ix509extensionkeyusage_initializeencode_method
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
 - IX509ExtensionKeyUsage.InitializeEncode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionKeyUsage::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the extension by using the <a href="https://msdn.microsoft.com/en-us/library/Aa379410(v=VS.85).aspx">X509KeyUsageFlags</a> enumeration. This method is web enabled.


## -parameters




### -param UsageFlags [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa379410(v=VS.85).aspx">X509KeyUsageFlags</a> enumeration value. This can be a bitwise-<b>OR</b> combination of any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE"></a><a id="xcn_cert_digital_signature_key_usage"></a><dl>
<dt><b>XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key is used with a <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Digital Signature Algorithm</a> (DSA) to support services other than nonrepudiation, certificate signing, or revocation list signing. DSAs are often used for authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_NON_REPUDIATION_KEY_USAGE"></a><a id="xcn_cert_non_repudiation_key_usage"></a><dl>
<dt><b>XCN_CERT_NON_REPUDIATION_KEY_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key is used to verify a digital signature as part of a nonrepudiation service that protects against false denial of action by a signing entity.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE"></a><a id="xcn_cert_key_encipherment_key_usage"></a><dl>
<dt><b>XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key is used for key transport. That is, the key is used to manage a key passed from its origination point to its point of actual use.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE"></a><a id="xcn_cert_data_encipherment_key_usage"></a><dl>
<dt><b>XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key is used to encrypt user data other than cryptographic keys.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_KEY_AGREEMENT_KEY_USAGE"></a><a id="xcn_cert_key_agreement_key_usage"></a><dl>
<dt><b>XCN_CERT_KEY_AGREEMENT_KEY_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key is used for key agreement. The key agreement or key exchange protocol enables two or more parties to negotiate a key value without transferring the key and without previously establishing a shared secret.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_KEY_CERT_SIGN_KEY_USAGE"></a><a id="xcn_cert_key_cert_sign_key_usage"></a><dl>
<dt><b>XCN_CERT_KEY_CERT_SIGN_KEY_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key is used to verify a certificate signature. This value can only be used for certificates issued by <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authorities</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_OFFLINE_CRL_SIGN_KEY_USAGE"></a><a id="xcn_cert_offline_crl_sign_key_usage"></a><dl>
<dt><b>XCN_CERT_OFFLINE_CRL_SIGN_KEY_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key is used to verify an offline <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate revocation list</a> (CRL) signature.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_CRL_SIGN_KEY_USAGE"></a><a id="xcn_cert_crl_sign_key_usage"></a><dl>
<dt><b>XCN_CERT_CRL_SIGN_KEY_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key is used to verify a CRL signature.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ENCIPHER_ONLY_KEY_USAGE"></a><a id="xcn_cert_encipher_only_key_usage"></a><dl>
<dt><b>XCN_CERT_ENCIPHER_ONLY_KEY_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key is used to encrypt data while performing key agreement. The <b>XCN_CERT_KEY_AGREEMENT_KEY_USAGE</b> value must also be specified.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_DECIPHER_ONLY_KEY_USAGE"></a><a id="xcn_cert_decipher_only_key_usage"></a><dl>
<dt><b>XCN_CERT_DECIPHER_ONLY_KEY_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key is used to decrypt data while performing key agreement. The <b>XCN_CERT_KEY_AGREEMENT_KEY_USAGE</b> value must also be specified.

</td>
</tr>
</table>
 


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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/en-us/library/Aa378146(v=VS.85).aspx">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/en-us/library/Aa378144(v=VS.85).aspx">IX509ExtensionKeyUsage</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct a <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) extension object from raw data, and the <b>InitializeDecode</b> method enables you to initialize the raw data from an encoded object.

You can retrieve the following properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property retrieves the extension <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID).</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378150(v=VS.85).aspx">KeyUsage</a> property retrieves the restrictions that identify the intended uses of the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key</a> (the raw extension data).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378144(v=VS.85).aspx">IX509ExtensionKeyUsage</a>
 

 

