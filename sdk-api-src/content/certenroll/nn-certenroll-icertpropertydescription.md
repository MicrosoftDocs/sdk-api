---
UID: NN:certenroll.ICertPropertyDescription
title: ICertPropertyDescription (certenroll.h)
description: Enables you to specify and retrieve a string that contains descriptive information for a certificate.
helpviewer_keywords: ["ICertPropertyDescription","ICertPropertyDescription interface [Security]","ICertPropertyDescription interface [Security]","described","certenroll/ICertPropertyDescription","security.icertpropertydescription"]
old-location: security\icertpropertydescription.htm
tech.root: security
ms.assetid: 229e8ce9-fe18-45f4-8f91-cd741052a134
ms.date: 12/05/2018
ms.keywords: ICertPropertyDescription, ICertPropertyDescription interface [Security], ICertPropertyDescription interface [Security],described, certenroll/ICertPropertyDescription, security.icertpropertydescription
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
 - ICertPropertyDescription
 - certenroll/ICertPropertyDescription
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
 - ICertPropertyDescription
---

# ICertPropertyDescription interface


## -description

The <b>ICertPropertyDescription</b> interface enables you to specify and retrieve a string that contains descriptive information for a  certificate. You can use this interface to identify the intended purpose of a certificate for display in a user interface.<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_DESCRIPTION_PROP_ID.</div>
<div> </div>

## -inheritance

The <b>ICertPropertyDescription</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyDescription</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyfriendlyname">ICertPropertyFriendlyName</a>
