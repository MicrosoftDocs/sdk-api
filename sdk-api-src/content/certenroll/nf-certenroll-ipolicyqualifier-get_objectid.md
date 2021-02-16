---
UID: NF:certenroll.IPolicyQualifier.get_ObjectId
title: IPolicyQualifier::get_ObjectId (certenroll.h)
description: Retrieves the object identifier (OID) for the qualifier.
helpviewer_keywords: ["IPolicyQualifier interface [Security]","ObjectId property","IPolicyQualifier.ObjectId","IPolicyQualifier.get_ObjectId","IPolicyQualifier::ObjectId","IPolicyQualifier::get_ObjectId","ObjectId property [Security]","ObjectId property [Security]","IPolicyQualifier interface","certenroll/IPolicyQualifier::ObjectId","certenroll/IPolicyQualifier::get_ObjectId","get_ObjectId","security.ipolicyqualifier_objectid_property"]
old-location: security\ipolicyqualifier_objectid_property.htm
tech.root: security
ms.assetid: d19efcd3-c5fc-4268-af39-2385b7babcc9
ms.date: 12/05/2018
ms.keywords: IPolicyQualifier interface [Security],ObjectId property, IPolicyQualifier.ObjectId, IPolicyQualifier.get_ObjectId, IPolicyQualifier::ObjectId, IPolicyQualifier::get_ObjectId, ObjectId property [Security], ObjectId property [Security],IPolicyQualifier interface, certenroll/IPolicyQualifier::ObjectId, certenroll/IPolicyQualifier::get_ObjectId, get_ObjectId, security.ipolicyqualifier_objectid_property
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
 - IPolicyQualifier::get_ObjectId
 - certenroll/IPolicyQualifier::get_ObjectId
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
 - IPolicyQualifier.ObjectId
 - IPolicyQualifier.get_ObjectId
---

# IPolicyQualifier::get_ObjectId


## -description

The <b>ObjectId</b> property retrieves the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for the qualifier.

This property is read-only.

## -parameters

## -remarks

If you specified <b>PolicyQualifierTypeUrl</b> in the <i>Type</i> parameter of the <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-initializeencode">InitializeEncode</a> method,  <b>XCN_OID_PKIX_POLICY_QUALIFIER_CPS</b> (1.3.6.1.5.5.7.2.1)  is returned. If you specified <b>PolicyQualifierTypeUserNotice</b>,  <b>XCN_OID_PKIX_POLICY_QUALIFIER_USERNOTICE</b> (1.3.6.1.5.5.7.2.2)  is returned.

You must call  <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-initializeencode">InitializeEncode</a> to initialize the qualifier object before you can retrieve this property. You can also retrieve the following properties for this object:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_qualifier">Qualifier</a> property retrieves the string specified for the <i>strQualifier</i> parameter of the <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-initializeencode">InitializeEncode</a> method.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_rawdata">RawData</a> property retrieves the <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded qualifier.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_type">Type</a> property retrieves a value of the <a href="/windows/desktop/api/certenroll/ne-certenroll-policyqualifiertype">PolicyQualifierType</a> enumeration that specifies the qualifier type.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a>