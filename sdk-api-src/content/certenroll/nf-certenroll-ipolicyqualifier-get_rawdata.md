---
UID: NF:certenroll.IPolicyQualifier.get_RawData
title: IPolicyQualifier::get_RawData (certenroll.h)
description: Retrieves the Distinguished Encoding Rules (DER) encoded qualifier object.
helpviewer_keywords: ["IPolicyQualifier interface [Security]","RawData property","IPolicyQualifier.RawData","IPolicyQualifier.get_RawData","IPolicyQualifier::RawData","IPolicyQualifier::get_RawData","RawData property [Security]","RawData property [Security]","IPolicyQualifier interface","certenroll/IPolicyQualifier::RawData","certenroll/IPolicyQualifier::get_RawData","get_RawData","security.ipolicyqualifier_rawdata_property"]
old-location: security\ipolicyqualifier_rawdata_property.htm
tech.root: security
ms.assetid: a654f60c-7f67-4fe2-847b-e8c5f91fde80
ms.date: 12/05/2018
ms.keywords: IPolicyQualifier interface [Security],RawData property, IPolicyQualifier.RawData, IPolicyQualifier.get_RawData, IPolicyQualifier::RawData, IPolicyQualifier::get_RawData, RawData property [Security], RawData property [Security],IPolicyQualifier interface, certenroll/IPolicyQualifier::RawData, certenroll/IPolicyQualifier::get_RawData, get_RawData, security.ipolicyqualifier_rawdata_property
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
 - IPolicyQualifier::get_RawData
 - certenroll/IPolicyQualifier::get_RawData
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
 - IPolicyQualifier.RawData
 - IPolicyQualifier.get_RawData
---

# IPolicyQualifier::get_RawData


## -description

The <b>RawData</b> property retrieves the <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded qualifier object.

This property is read-only.

## -parameters

## -remarks

You must call  <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-initializeencode">InitializeEncode</a> to initialize the qualifier object before you can retrieve this property. The value retrieved is the DER-encoded byte array that contains the qualifier. The byte array is represented as a string. You can use the <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration to apply Unicode encoding to the string.

You can also retrieve the following properties for this object:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_objectid">ObjectId</a> property retrieves an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that identifies whether the qualifier is a CPS or a user notice.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_qualifier">Qualifier</a> property retrieves the string specified for the <i>strQualifier</i> parameter of the <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-initializeencode">InitializeEncode</a> method.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifier-get_type">Type</a> property retrieves a value of the <a href="/windows/desktop/api/certenroll/ne-certenroll-policyqualifiertype">PolicyQualifierType</a> enumeration that specifies the qualifier type.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a>