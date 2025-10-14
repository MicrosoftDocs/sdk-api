---
UID: NF:certenroll.IObjectId.GetAlgorithmName
title: IObjectId::GetAlgorithmName (certenroll.h)
description: Retrieves the display name associated with an algorithm object identifier (OID).
helpviewer_keywords: ["GetAlgorithmName","GetAlgorithmName method [Security]","GetAlgorithmName method [Security]","IObjectId interface","IObjectId interface [Security]","GetAlgorithmName method","IObjectId.GetAlgorithmName","IObjectId::GetAlgorithmName","certenroll/IObjectId::GetAlgorithmName","security.iobjectid_getalgorithmname"]
old-location: security\iobjectid_getalgorithmname.htm
tech.root: security
ms.assetid: 3d24d658-1016-4e63-8d93-5db0a3144121
ms.date: 12/05/2018
ms.keywords: GetAlgorithmName, GetAlgorithmName method [Security], GetAlgorithmName method [Security],IObjectId interface, IObjectId interface [Security],GetAlgorithmName method, IObjectId.GetAlgorithmName, IObjectId::GetAlgorithmName, certenroll/IObjectId::GetAlgorithmName, security.iobjectid_getalgorithmname
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
 - IObjectId::GetAlgorithmName
 - certenroll/IObjectId::GetAlgorithmName
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
 - IObjectId.GetAlgorithmName
---

# IObjectId::GetAlgorithmName


## -description

The <b>GetAlgorithmName</b> method retrieves the display name associated with an algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

## -parameters

### -param GroupId [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-objectidgroupid">ObjectIdGroupId</a> enumeration value that specifies the OID group to search. This can be any of the following algorithm groups:

<ul>
<li><b>XCN_CRYPT_HASH_ALG_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_SIGN_ALG_OID_GROUP_ID</b></li>
</ul>
In addition, you can also specify groups that do not contain cryptographic algorithms:

<ul>
<li><b>XCN_CRYPT_RDN_ATTR_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_EXT_OR_ATTR_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_ENHKEY_USAGE_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_POLICY_OID_GROUP_ID</b></li>
<li><b>XCN_CRYPT_TEMPLATE_OID_GROUP_ID</b></li>
</ul>

### -param KeyFlags [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-objectidpublickeyflags">ObjectIdPublicKeyFlags</a> enumeration value that specifies whether to search for a signing or an encryption algorithm. This can be one of the following values:<ul>
<li><b>XCN_CRYPT_OID_INFO_PUBKEY_ANY</b></li>
<li><b>XCN_CRYPT_OID_INFO_PUBKEY_SIGN_KEY_FLAG</b></li>
<li><b>XCN_CRYPT_OID_INFO_PUBKEY_ENCRYPT_KEY_FLAG</b></li>
</ul>You can use either of the last two values to disambiguate among algorithms such as RSA that can be used to both encrypt and sign messages. You must also specify <b>XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID</b> in the <i>GroupId</i> parameter. Specify <b>XCN_CRYPT_OID_INFO_PUBKEY_ANY</b> if you set the <i>GroupId</i> parameter to anything other than <b>XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID</b>.

### -param pstrAlgorithmName [out]

Pointer to a <b>BSTR</b> variable that contains the name.

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
The string that contains the algorithm name is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The algorithm name could not be found. You must call <a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromalgorithmname">InitializeFromAlgorithmName</a> before calling <a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-getalgorithmname">GetAlgorithmName</a>.

</td>
</tr>
</table>

## -remarks

You can use the <b>XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID</b> constant to create a <i>GroupId</i> parameter value that takes account of the key size for algorithms that can be identified by a variable bit length. For example, to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> object from a 192-bit AES algorithm, specify "AES" for the <i>strAlgorithmName</i> parameter, shift the length left by 16, and perform a bitwise-OR combination on the shifted bit length and <b>XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID</b>.

If you set the <i>GroupId</i> parameter to anything other than <b>XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID</b>, specify <b>XCN_CRYPT_OID_INFO_PUBKEY_ANY</b> for the <i>KeyFlags</i> parameter.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a>