---
UID: NF:certenroll.IPolicyQualifier.get_Type
title: IPolicyQualifier::get_Type (certenroll.h)
description: Retrieves the qualifier type.
helpviewer_keywords: ["IPolicyQualifier interface [Security]","Type property","IPolicyQualifier.Type","IPolicyQualifier.get_Type","IPolicyQualifier::Type","IPolicyQualifier::get_Type","Type property [Security]","Type property [Security]","IPolicyQualifier interface","certenroll/IPolicyQualifier::Type","certenroll/IPolicyQualifier::get_Type","get_Type","security.ipolicyqualifier_type_property"]
old-location: security\ipolicyqualifier_type_property.htm
tech.root: security
ms.assetid: eb48d2a0-c689-45b1-9f06-83df71987b4b
ms.date: 12/05/2018
ms.keywords: IPolicyQualifier interface [Security],Type property, IPolicyQualifier.Type, IPolicyQualifier.get_Type, IPolicyQualifier::Type, IPolicyQualifier::get_Type, Type property [Security], Type property [Security],IPolicyQualifier interface, certenroll/IPolicyQualifier::Type, certenroll/IPolicyQualifier::get_Type, get_Type, security.ipolicyqualifier_type_property
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
 - IPolicyQualifier::get_Type
 - certenroll/IPolicyQualifier::get_Type
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
 - IPolicyQualifier.Type
 - IPolicyQualifier.get_Type
---

# IPolicyQualifier::get_Type


## -description

The <b>Type</b> property retrieves the qualifier type.

This property is read-only.

## -parameters

## -remarks

You must call  <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-initializeencode">InitializeEncode</a> to initialize the qualifier object before you can retrieve this property. The value retrieved is one of the following  values of the <a href="/windows/desktop/api/certenroll/ne-certenroll-policyqualifiertype">PolicyQualifierType</a> enumeration.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>PolicyQualifierTypeUrl</b></td>
<td>The qualifier is a URL that points to a Certification Practice Statement (CPS).</td>
</tr>
<tr>
<td><b>PolicyQualifierTypeUserNotice</b></td>
<td>The qualifier is a string to be displayed to users who rely on the certificate.</td>
</tr>
</table>
 



You can also retrieve the following properties for this object:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_objectid">ObjectId</a> property retrieves an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that identifies whether the qualifier is a CPS or a user notice.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_qualifier">Qualifier</a> property retrieves the string specified for the <i>strQualifier</i> parameter of the <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-initializeencode">InitializeEncode</a> method.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_rawdata">RawData</a> property retrieves the <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded qualifier.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a>