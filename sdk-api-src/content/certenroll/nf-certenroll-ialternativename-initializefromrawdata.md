---
UID: NF:certenroll.IAlternativeName.InitializeFromRawData
title: IAlternativeName::InitializeFromRawData (certenroll.h)
description: Initializes the object from a Digital Signature Algorithm (DSA) GUID, an X.500 directory name, or an Internet Protocol (IP) address contained in a Distinguished Encoding Rules (DER) encoded byte array.
helpviewer_keywords: ["IAlternativeName interface [Security]","InitializeFromRawData method","IAlternativeName.InitializeFromRawData","IAlternativeName::InitializeFromRawData","InitializeFromRawData","InitializeFromRawData method [Security]","InitializeFromRawData method [Security]","IAlternativeName interface","XCN_CERT_ALT_NAME_DIRECTORY_NAME","XCN_CERT_ALT_NAME_GUID","XCN_CERT_ALT_NAME_IP_ADDRESS","certenroll/IAlternativeName::InitializeFromRawData","security.ialternativename_initializefromrawdata_method"]
old-location: security\ialternativename_initializefromrawdata_method.htm
tech.root: security
ms.assetid: 1559801c-ec62-471e-851f-f67219565cd1
ms.date: 12/05/2018
ms.keywords: IAlternativeName interface [Security],InitializeFromRawData method, IAlternativeName.InitializeFromRawData, IAlternativeName::InitializeFromRawData, InitializeFromRawData, InitializeFromRawData method [Security], InitializeFromRawData method [Security],IAlternativeName interface, XCN_CERT_ALT_NAME_DIRECTORY_NAME, XCN_CERT_ALT_NAME_GUID, XCN_CERT_ALT_NAME_IP_ADDRESS, certenroll/IAlternativeName::InitializeFromRawData, security.ialternativename_initializefromrawdata_method
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
 - IAlternativeName::InitializeFromRawData
 - certenroll/IAlternativeName::InitializeFromRawData
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
 - IAlternativeName.InitializeFromRawData
---

# IAlternativeName::InitializeFromRawData


## -description

The <b>InitializeFromRawData</b> method initializes the object from a <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Algorithm</a> (DSA) GUID, an <a href="/windows/desktop/SecGloss/x-gly">X.500</a> directory name, or an Internet Protocol (IP) address contained in a <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array.

## -parameters

### -param Type [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-alternativenametype">AlternativeNameType</a> enumeration value that identifies the type of name represented by the input string. This must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_DIRECTORY_NAME"></a><a id="xcn_cert_alt_name_directory_name"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_DIRECTORY_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is an X.500 directory name.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_IP_ADDRESS"></a><a id="xcn_cert_alt_name_ip_address"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_IP_ADDRESS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is an IP address.

</td>
</tr>
<tr>
<td width="40%"><a id="XCN_CERT_ALT_NAME_GUID"></a><a id="xcn_cert_alt_name_guid"></a><dl>
<dt><b>XCN_CERT_ALT_NAME_GUID</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The name is a GUID.

</td>
</tr>
</table>

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that identifies the type of Unicode encoding applied to the <i>strRawData</i> parameter.

### -param strRawData [in]

A <b>BSTR</b> variable that contains the DER-encoded data.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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

The raw data is a byte array that has been encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER). You must specify the  byte array as a Unicode encoded string.

If you use this method to specify a DSA GUID (XCN_CERT_ALT_NAME_GUID), the GUID is associated with the XCN_OID_NTDS_REPLICATION (1.3.6.1.4.1.311.25.1) <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and encoded as an octet string (byte array). You can retrieve the OID by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ialternativename-get_objectid">ObjectId</a> property. You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ialternativename-get_rawdata">RawData</a> property to retrieve the encoded byte array.

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
<td>XCN_CERT_ALT_NAME_RFC822_NAME</td>
<td>The name is an email address.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DNS_NAME</td>
<td>The name is a DNS name.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_URL</td>
<td>The name is a URL.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_REGISTERED_ID</td>
<td>The name is a registered OID.</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME</td>
<td>The name is a <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN).</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_OTHER_NAME</td>
<td>The name consists of an OID and a byte array.</td>
</tr>
</table>
 



You can use the <a href="/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromothername">InitializeFromOtherName</a> method to specify an OID and a corresponding name string, and you can use the <a href="/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromstring">InitializeFromString</a> method to specify an email address, a DNS name, a URL, a registered OID, or a <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN).

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a>