---
UID: NF:certenroll.IPolicyQualifier.get_Qualifier
title: IPolicyQualifier::get_Qualifier (certenroll.h)
description: Retrieves a string that contains the qualifier used to initialize the object.
helpviewer_keywords: ["IPolicyQualifier interface [Security]","Qualifier property","IPolicyQualifier.Qualifier","IPolicyQualifier.get_Qualifier","IPolicyQualifier::Qualifier","IPolicyQualifier::get_Qualifier","Qualifier property [Security]","Qualifier property [Security]","IPolicyQualifier interface","certenroll/IPolicyQualifier::Qualifier","certenroll/IPolicyQualifier::get_Qualifier","get_Qualifier","security.ipolicyqualifier_qualifier_property"]
old-location: security\ipolicyqualifier_qualifier_property.htm
tech.root: security
ms.assetid: 73cecc9b-519c-45c8-b9f8-864ff628560a
ms.date: 12/05/2018
ms.keywords: IPolicyQualifier interface [Security],Qualifier property, IPolicyQualifier.Qualifier, IPolicyQualifier.get_Qualifier, IPolicyQualifier::Qualifier, IPolicyQualifier::get_Qualifier, Qualifier property [Security], Qualifier property [Security],IPolicyQualifier interface, certenroll/IPolicyQualifier::Qualifier, certenroll/IPolicyQualifier::get_Qualifier, get_Qualifier, security.ipolicyqualifier_qualifier_property
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
 - IPolicyQualifier::get_Qualifier
 - certenroll/IPolicyQualifier::get_Qualifier
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
 - IPolicyQualifier.Qualifier
 - IPolicyQualifier.get_Qualifier
---

# IPolicyQualifier::get_Qualifier


## -description

The <b>Qualifier</b> property retrieves a string that contains the qualifier used to initialize the object.

This property is read-only.

## -parameters

## -remarks

You must call  <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-initializeencode">InitializeEncode</a> to initialize the qualifier object before you can retrieve this property. The value retrieved is the string entered in the <i>strQualifier</i> parameter of that method. You can also retrieve the following properties for this object:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_objectid">ObjectId</a> property retrieves an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that identifies whether the qualifier is a CPS or a user notice.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_rawdata">RawData</a> property retrieves the <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded qualifier.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_type">Type</a> property retrieves a value of the <a href="/windows/desktop/api/certenroll/ne-certenroll-policyqualifiertype">PolicyQualifierType</a> enumeration that specifies the qualifier type.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a>