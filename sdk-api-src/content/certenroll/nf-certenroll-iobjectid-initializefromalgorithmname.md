---
UID: NF:certenroll.IObjectId.InitializeFromAlgorithmName
title: IObjectId::InitializeFromAlgorithmName (certenroll.h)
description: Initializes the object from an algorithm name or an object identifier.
helpviewer_keywords: ["IObjectId interface [Security]","InitializeFromAlgorithmName method","IObjectId.InitializeFromAlgorithmName","IObjectId::InitializeFromAlgorithmName","InitializeFromAlgorithmName","InitializeFromAlgorithmName method [Security]","InitializeFromAlgorithmName method [Security]","IObjectId interface","certenroll/IObjectId::InitializeFromAlgorithmName","security.iobjectid_initializefromalgorithmname_method"]
old-location: security\iobjectid_initializefromalgorithmname_method.htm
tech.root: security
ms.assetid: ba8c1f11-9380-43a9-b444-b0fff114a176
ms.date: 12/05/2018
ms.keywords: IObjectId interface [Security],InitializeFromAlgorithmName method, IObjectId.InitializeFromAlgorithmName, IObjectId::InitializeFromAlgorithmName, InitializeFromAlgorithmName, InitializeFromAlgorithmName method [Security], InitializeFromAlgorithmName method [Security],IObjectId interface, certenroll/IObjectId::InitializeFromAlgorithmName, security.iobjectid_initializefromalgorithmname_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjectId::InitializeFromAlgorithmName
 - certenroll/IObjectId::InitializeFromAlgorithmName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IObjectId.InitializeFromAlgorithmName
---

# IObjectId::InitializeFromAlgorithmName


## -description

The <b>InitializeFromAlgorithmName</b> method initializes the object from an algorithm name or an object identifier. This method has been provided primarily to enable you to initialize the object from a Cryptography API: Next Generation (CNG) algorithm name. You can, however, specify any OID name. This method is web enabled.

## -parameters

### -param GroupId [in]

An  <a href="/windows/desktop/api/certenroll/ne-certenroll-objectidgroupid">ObjectIdGroupId</a> enumeration value that specifies the OID group to search. This can be any of the following algorithm groups:<ul>
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

An <a href="/windows/desktop/api/certenroll/ne-certenroll-objectidpublickeyflags">ObjectIdPublicKeyFlags</a> enumeration value that specifies whether to search for a signing or an encryption algorithm. This can be one of the following values:<ul>
<li><b>XCN_CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG</b></li>
<li><b>XCN_CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG</b></li>
</ul>You can use either value to disambiguate among algorithms such as RSA that can be used to both encrypt and sign messages. You must also specify <b>XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID</b> in the <i>GroupId</i> parameter.

### -param AlgFlags [in]

An  <a href="/windows/desktop/api/certenroll/ne-certenroll-algorithmflags">AlgorithmFlags</a> enumeration value. This can be one of the following values:

<ul>
<li><b>AlgorithmFlagsNone</b></li>
<li><b>AlgorithmFlagsWrap</b></li>
</ul>
If you specify <b>XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID</b> for the <i>GroupId</i> parameter, you can use the <b>AlgorithmFlags</b> enumeration to search for an OID that can be used to wrap a key. For example, you can retrieve information about the AES128wrap algorithm if you specify a bit length of 128 (see the Remarks section), set the <i>strAlgorithmName</i> parameter to AES, and specify <b>AlgorithmFlagsWrap</b>.

### -param strAlgorithmName [in]

A <b>BSTR</b> variable that contains the name. You can specify a name, or an OID in dotted decimal format.  The method verifies that the format is consistent with the ASN.1 X.208 standard. For more information about CNG algorithm names, see <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a>.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
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
<dt><b>CRYPT_E_UNKNOWN_ALGO</b></dt>
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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>

## -remarks

You can use the upper 16 bits of the <i>GroupId</i> parameter to specify the key size for algorithms that accept a variable bit length. For example, to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> object from a 192-bit AES algorithm, specify "AES" for the <i>strAlgorithmName</i> parameter, shift the length left by 16, and perform a bitwise-<b>OR</b> combination on the shifted bit length and the <i>GroupId</i> value.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a>