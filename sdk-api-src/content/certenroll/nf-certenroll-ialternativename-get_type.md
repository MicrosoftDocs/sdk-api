---
UID: NF:certenroll.IAlternativeName.get_Type
title: IAlternativeName::get_Type (certenroll.h)
description: Retrieves the alternative name type.
helpviewer_keywords: ["IAlternativeName interface [Security]","Type property","IAlternativeName.Type","IAlternativeName.get_Type","IAlternativeName::Type","IAlternativeName::get_Type","Type property [Security]","Type property [Security]","IAlternativeName interface","certenroll/IAlternativeName::Type","certenroll/IAlternativeName::get_Type","get_Type","security.ialternativename_type_property"]
old-location: security\ialternativename_type_property.htm
tech.root: security
ms.assetid: fdb1a7db-20f6-4732-bb59-fc078387375d
ms.date: 12/05/2018
ms.keywords: IAlternativeName interface [Security],Type property, IAlternativeName.Type, IAlternativeName.get_Type, IAlternativeName::Type, IAlternativeName::get_Type, Type property [Security], Type property [Security],IAlternativeName interface, certenroll/IAlternativeName::Type, certenroll/IAlternativeName::get_Type, get_Type, security.ialternativename_type_property
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
 - IAlternativeName::get_Type
 - certenroll/IAlternativeName::get_Type
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
 - IAlternativeName.Type
 - IAlternativeName.get_Type
---

# IAlternativeName::get_Type


## -description

The <b>Type</b> property retrieves the alternative name type.

This property is read-only.

## -parameters

## -remarks

The following values from the <a href="/windows/desktop/api/certenroll/ne-certenroll-alternativenametype">AlternativeNameType</a> enumeration can be returned. The  <b>XCN_CERT_ALT_NAME_UNKNOWN</b> value is never returned.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>XCN_CERT_ALT_NAME_OTHER_NAME</b></td>
<td>The name consists of an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and a byte array.</td>
</tr>
<tr>
<td><b>XCN_CERT_ALT_NAME_RFC822_NAME</b></td>
<td>The name is an email address.</td>
</tr>
<tr>
<td><b>XCN_CERT_ALT_NAME_DNS_NAME</b></td>
<td>The name is a DNS name.</td>
</tr>
<tr>
<td><b>XCN_CERT_ALT_NAME_DIRECTORY_NAME</b></td>
<td>The name is an <a href="/windows/desktop/SecGloss/x-gly">X.500</a> directory name.</td>
</tr>
<tr>
<td><b>XCN_CERT_ALT_NAME_URL</b></td>
<td>The name is a URL.</td>
</tr>
<tr>
<td><b>XCN_CERT_ALT_NAME_IP_ADDRESS</b></td>
<td>The name is an IP address.</td>
</tr>
<tr>
<td><b>XCN_CERT_ALT_NAME_REGISTERED_ID</b></td>
<td>The name is a registered OID.</td>
</tr>
<tr>
<td><b>XCN_CERT_ALT_NAME_GUID</b></td>
<td>The name is a GUID.</td>
</tr>
<tr>
<td><b>XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME</b></td>
<td>The name is a <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN).</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a>