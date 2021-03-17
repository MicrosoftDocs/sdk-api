---
UID: NF:certenroll.IAlternativeName.InitializeFromString
title: IAlternativeName::InitializeFromString (certenroll.h)
description: Initializes the object from a string that contains an email address, a Domain Name System (DNS) name, a URL, a registered object identifier (OID), or a user principal name (UPN).
helpviewer_keywords: ["IAlternativeName interface [Security]","InitializeFromString method","IAlternativeName.InitializeFromString","IAlternativeName::InitializeFromString","InitializeFromString","InitializeFromString method [Security]","InitializeFromString method [Security]","IAlternativeName interface","XCN_CERT_ALT_NAME_DNS_NAME","XCN_CERT_ALT_NAME_REGISTERED_ID","XCN_CERT_ALT_NAME_RFC822_NAME","XCN_CERT_ALT_NAME_URL","XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME","certenroll/IAlternativeName::InitializeFromString","security.ialternativename_initializefromstring_method"]
old-location: security\ialternativename_initializefromstring_method.htm
tech.root: security
ms.assetid: 7b5f7dd3-00dc-474b-8920-45a3acded209
ms.date: 12/05/2018
ms.keywords: IAlternativeName interface [Security],InitializeFromString method, IAlternativeName.InitializeFromString, IAlternativeName::InitializeFromString, InitializeFromString, InitializeFromString method [Security], InitializeFromString method [Security],IAlternativeName interface, XCN_CERT_ALT_NAME_DNS_NAME, XCN_CERT_ALT_NAME_REGISTERED_ID, XCN_CERT_ALT_NAME_RFC822_NAME, XCN_CERT_ALT_NAME_URL, XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME, certenroll/IAlternativeName::InitializeFromString, security.ialternativename_initializefromstring_method
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
 - IAlternativeName::InitializeFromString
 - certenroll/IAlternativeName::InitializeFromString
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
 - IAlternativeName.InitializeFromString
---

# IAlternativeName::InitializeFromString


## -description

The <b>InitializeFromString</b> method initializes the object from a string that contains an email address, a Domain Name System (DNS) name, a URL, a registered <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID), or a <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN).

## -parameters

### -param Type [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-alternativenametype">AlternativeNameType</a> enumeration value that identifies the type of name represented by the input string contained in the <i>strValue</i> parameter. This must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_RFC822_NAME"></a><a id="xcn_cert_alt_name_rfc822_name"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_RFC822_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is an email address.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_DNS_NAME"></a><a id="xcn_cert_alt_name_dns_name"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_DNS_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is a DNS name.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_URL"></a><a id="xcn_cert_alt_name_url"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_URL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is a URL.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_REGISTERED_ID"></a><a id="xcn_cert_alt_name_registered_id"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_REGISTERED_ID</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is a registered OID.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME"></a><a id="xcn_cert_alt_name_user_principle_name"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is a UPN.

</td>
</tr>
</table>

### -param strValue [in]

A <b>BSTR</b> variable that contains the name.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If you use this method to specify a UPN, the UPN is associated with the XCN_OID_NT_PRINCIPAL_NAME (1.3.6.1.4.1.311.20.2.3) OID and is <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded. You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ialternativename-get_rawdata">RawData</a> property to retrieve the encoded byte array. You can retrieve the OID by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ialternativename-get_objectid">ObjectId</a> property.

If you use this method to specify any of the following name types, the method returns <b>E_INVALIDARG</b>.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_UNKNOWN</td>
<td>The name type is not identified.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_OTHER_NAME</td>
<td>The name consists of an OID and a byte array.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DIRECTORY_NAME</td>
<td>The name is an <a href="/windows/desktop/SecGloss/x-gly">X.500</a> directory name.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_IP_ADDRESS</td>
<td>The name is an IP address.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_GUID</td>
<td>The name is a GUID.</td>
</tr>
</table>
 



You can use the <a href="/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromothername">InitializeFromOtherName</a> method to specify an OID and a corresponding name string, and you can use the <a href="/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromrawdata">InitializeFromRawData</a> method to specify a GUID, IP address, or X.500 directory name.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativenames">IAlternativeNames</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionalternativenames">IX509ExtensionAlternativeNames</a>