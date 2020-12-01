---
UID: NF:certenroll.IObjectId.get_Value
title: IObjectId::get_Value (certenroll.h)
description: Retrieves a string that contains the dotted decimal object identifier (OID).
helpviewer_keywords: ["IObjectId interface [Security]","Value property","IObjectId.Value","IObjectId.get_Value","IObjectId::Value","IObjectId::get_Value","Value property [Security]","Value property [Security]","IObjectId interface","certenroll/IObjectId::Value","certenroll/IObjectId::get_Value","get_Value","security.iobjectid_value_property"]
old-location: security\iobjectid_value_property.htm
tech.root: security
ms.assetid: 9ccb681a-f31b-4d31-ae56-25efd2af2b2c
ms.date: 12/05/2018
ms.keywords: IObjectId interface [Security],Value property, IObjectId.Value, IObjectId.get_Value, IObjectId::Value, IObjectId::get_Value, Value property [Security], Value property [Security],IObjectId interface, certenroll/IObjectId::Value, certenroll/IObjectId::get_Value, get_Value, security.iobjectid_value_property
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
 - IObjectId::get_Value
 - certenroll/IObjectId::get_Value
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
 - IObjectId.Value
 - IObjectId.get_Value
---

# IObjectId::get_Value


## -description

The <b>Value</b> property retrieves a string that contains the dotted decimal <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). This property is web enabled.

This property is read-only.

## -parameters

## -remarks

The dotted decimal format is discussed in the ASN.1 X.208 specification. For example, the string 1.2.840.10045.4.1. represents the iso(1)member-body(2)us(840)10045 signatures(4)sha1(1) object identifier.

You must call any of the following methods before you can retrieve this property value:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromalgorithmname">InitializeFromAlgorithmName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromname">InitializeFromName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromvalue">InitializeFromValue</a>
</li>
</ul>


You can also retrieve the following property values:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-get_friendlyname">FriendlyName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-get_name">Name</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectID</a>