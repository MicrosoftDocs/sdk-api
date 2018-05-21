---
UID: NF:certenroll.IObjectId.InitializeFromAlgorithmName
title: IObjectId::InitializeFromAlgorithmName
author: windows-driver-content
description: Initializes the object from an algorithm name or an object identifier.
old-location: security\iobjectid_initializefromalgorithmname_method.htm
old-project: SecCertEnroll
ms.assetid: ba8c1f11-9380-43a9-b444-b0fff114a176
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IObjectId interface [Security],InitializeFromAlgorithmName method, IObjectId.InitializeFromAlgorithmName, IObjectId::InitializeFromAlgorithmName, InitializeFromAlgorithmName, InitializeFromAlgorithmName method [Security], InitializeFromAlgorithmName method [Security],IObjectId interface, certenroll/IObjectId::InitializeFromAlgorithmName, security.iobjectid_initializefromalgorithmname_method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IObjectId.InitializeFromAlgorithmName
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IObjectId::InitializeFromAlgorithmName


## -description


The <b>InitializeFromAlgorithmName</b> method initializes the object from an algorithm name or an object identifier. This method has been provided primarily to enable you to initialize the object from a Cryptography API: Next Generation (CNG) algorithm name. You can, however, specify any OID name. This method is web enabled.


## -parameters




### -param GroupId [in]

An  <a href="https://msdn.microsoft.com/66a70cad-ce72-461b-8d71-605a62dd35b4">ObjectIdGroupId</a> enumeration value that specifies the OID group to search. This can be any of the following algorithm groups:<ul>
<li><b>XCN_CRYPT_HASH_ALG_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_SIGN_ALG_OID_GROUP_ID</b></li>
</ul>In addition, you can also specify groups that do not contain cryptographic algorithms:<ul>
<li><b>XCN_CRYPT_RDN_ATTR_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_EXT_OR_ATTR_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_ENHKEY_USAGE_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_POLICY_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_TEMPLATE_OID_GROUP_ID</b></li>
</ul>



### -param KeyFlags [in]

An <a href="https://msdn.microsoft.com/f41a871a-0247-4c49-b6a0-66d31c54a0e3">ObjectIdPublicKeyFlags</a> enumeration value that specifies whether to search for a signing or an encryption algorithm. This can be one of the following values:<ul>
<li><b>XCN_CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG</b></li>
<li><b>XCN_CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG</b></li>
</ul>You can use either value to disambiguate among algorithms such as RSA that can be used to both encrypt and sign messages. You must also specify <b>XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID</b> in the <i>GroupId</i> parameter.


### -param AlgFlags [in]

An  <a href="https://msdn.microsoft.com/0f067687-ae92-4500-af19-80f537620bb9">AlgorithmFlags</a> enumeration value. This can be one of the following values:

<ul>
<li><b>AlgorithmFlagsNone</b></li>
<li><b>AlgorithmFlagsWrap</b></li>
</ul>
If you specify <b>XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID</b> for the <i>GroupId</i> parameter, you can use the <b>AlgorithmFlags</b> enumeration to search for an OID that can be used to wrap a key. For example, you can retrieve information about the AES128wrap algorithm if you specify a bit length of 128 (see the Remarks section), set the <i>strAlgorithmName</i> parameter to AES, and specify <b>AlgorithmFlagsWrap</b>.


### -param strAlgorithmName [in]

A <b>BSTR</b> variable that contains the name. You can specify a name, or an OID in dotted decimal format.  The method verifies that the format is consistent with the ASN.1 X.208 standard. For more information about CNG algorithm names, see <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a>.


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
The OID information could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CRYPT_E_UNKNOWN_ALGO</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The algorithm name is not recognized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



You can use the upper 16 bits of the <i>GroupId</i> parameter to specify the key size for algorithms that accept a variable bit length. For example, to initialize an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> object from a 192-bit AES algorithm, specify "AES" for the <i>strAlgorithmName</i> parameter, shift the length left by 16, and perform a bitwise-<b>OR</b> combination on the shifted bit length and the <i>GroupId</i> value.




## -see-also




<a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a>
 

 

