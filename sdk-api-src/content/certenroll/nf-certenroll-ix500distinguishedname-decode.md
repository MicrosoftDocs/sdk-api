---
UID: NF:certenroll.IX500DistinguishedName.Decode
title: IX500DistinguishedName::Decode (certenroll.h)
description: Initializes the object from a Unicode-encoded distinguished name.
helpviewer_keywords: ["Decode","Decode method [Security]","Decode method [Security]","IX500DistinguishedName interface","IX500DistinguishedName interface [Security]","Decode method","IX500DistinguishedName.Decode","IX500DistinguishedName::Decode","certenroll/IX500DistinguishedName::Decode","security.ix500distinguishedname_decode_method"]
old-location: security\ix500distinguishedname_decode_method.htm
tech.root: security
ms.assetid: 52cc0595-b825-4bf3-805c-21afc468b91e
ms.date: 12/05/2018
ms.keywords: Decode, Decode method [Security], Decode method [Security],IX500DistinguishedName interface, IX500DistinguishedName interface [Security],Decode method, IX500DistinguishedName.Decode, IX500DistinguishedName::Decode, certenroll/IX500DistinguishedName::Decode, security.ix500distinguishedname_decode_method
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
 - IX500DistinguishedName::Decode
 - certenroll/IX500DistinguishedName::Decode
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
 - IX500DistinguishedName.Decode
---

# IX500DistinguishedName::Decode


## -description

The <b>Decode</b> method initializes the object from a Unicode-encoded distinguished name.

## -parameters

### -param strEncodedName [in]

A <b>BSTR</b> variable that contains the encoded name.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the input string. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.

### -param NameFlags [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x500nameflags">X500NameFlags</a> enumeration value that specifies the format of the decoded string.

<div class="alert"><b>Note</b>  The following flags are set automatically:<ul>
<li>The default value specified in Certenroll.h is <b>XCN_CERT_NAME_STR_NONE</b>.</li>
<li>If you do not specify XCN_CERT_NAME_STR_FORWARD_FLAG, then XCN_CERT_NAME_STR_REVERSE_FLAG is automatically applied.</li>
<li>If you do not specify XCN_CERT_NAME_STR_DISABLE_UTF8_DIR_STR_FLAG, then XCN_CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG is automatically applied.</li>
<li>XCN_CERT_NAME_STR_ENABLE_PUNYCODE_FLAG is automatically set regardless of any other flag you specify.</li>
</ul>
</div>
<div> </div>

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated for the decoded value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <i>strEncodedName</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name could not be decoded.

</td>
</tr>
</table>

## -remarks

This method internally calls the CryptoAPI <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a> function. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix500distinguishedname-get_name">Name</a> property to retrieve the name as a null-terminated character string. Call the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix500distinguishedname-get_encodedname">EncodedName</a> property to retrieve a string containing an encoded name.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix500distinguishedname">IX500DistinguishedName</a>