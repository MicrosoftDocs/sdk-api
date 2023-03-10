---
UID: NF:certenroll.IAlternativeName.get_StrValue
title: IAlternativeName::get_StrValue (certenroll.h)
description: Retrieves a string that contains an email address, a Domain Name System (DNS) name, a URL, a registered object identifier (OID), or a user principal name (UPN).
helpviewer_keywords: ["IAlternativeName interface [Security]","StrValue property","IAlternativeName.StrValue","IAlternativeName.get_StrValue","IAlternativeName::StrValue","IAlternativeName::get_StrValue","StrValue property [Security]","StrValue property [Security]","IAlternativeName interface","certenroll/IAlternativeName::StrValue","certenroll/IAlternativeName::get_StrValue","get_StrValue","security.ialternativename_strvalue_property"]
old-location: security\ialternativename_strvalue_property.htm
tech.root: security
ms.assetid: 1d916450-4a4e-4f11-b95b-dbf9693b7cdd
ms.date: 12/05/2018
ms.keywords: IAlternativeName interface [Security],StrValue property, IAlternativeName.StrValue, IAlternativeName.get_StrValue, IAlternativeName::StrValue, IAlternativeName::get_StrValue, StrValue property [Security], StrValue property [Security],IAlternativeName interface, certenroll/IAlternativeName::StrValue, certenroll/IAlternativeName::get_StrValue, get_StrValue, security.ialternativename_strvalue_property
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
 - IAlternativeName::get_StrValue
 - certenroll/IAlternativeName::get_StrValue
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
 - IAlternativeName.StrValue
 - IAlternativeName.get_StrValue
---

# IAlternativeName::get_StrValue


## -description

The <b>StrValue</b> property retrieves a string that contains an email address, a Domain Name System (DNS) name, a URL, a registered <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID), or a <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN).

This property is read-only.

## -parameters

## -remarks

You can call this property to retrieve a string if you initialized the <a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a> object by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromstring">InitializeFromString</a> method and specifying one of the following <a href="/windows/desktop/api/certenroll/ne-certenroll-alternativenametype">AlternativeNameType</a> values.<table>
<tr>
<th>Value</th>
<th>Description</th>
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
<td>The name is a UPN.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a>