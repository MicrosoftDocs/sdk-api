---
UID: NF:certenroll.ISmimeCapability.get_ObjectId
title: ISmimeCapability::get_ObjectId (certenroll.h)
description: Retrieves the object identifier (OID) of the symmetric encryption algorithm.
helpviewer_keywords: ["ISmimeCapability interface [Security]","ObjectId property","ISmimeCapability.ObjectId","ISmimeCapability.get_ObjectId","ISmimeCapability::ObjectId","ISmimeCapability::get_ObjectId","ObjectId property [Security]","ObjectId property [Security]","ISmimeCapability interface","certenroll/ISmimeCapability::ObjectId","certenroll/ISmimeCapability::get_ObjectId","get_ObjectId","security.ismimecapability_objectid_property"]
old-location: security\ismimecapability_objectid_property.htm
tech.root: security
ms.assetid: 3bd773f2-f3ea-45e5-9b37-8346070049d8
ms.date: 12/05/2018
ms.keywords: ISmimeCapability interface [Security],ObjectId property, ISmimeCapability.ObjectId, ISmimeCapability.get_ObjectId, ISmimeCapability::ObjectId, ISmimeCapability::get_ObjectId, ObjectId property [Security], ObjectId property [Security],ISmimeCapability interface, certenroll/ISmimeCapability::ObjectId, certenroll/ISmimeCapability::get_ObjectId, get_ObjectId, security.ismimecapability_objectid_property
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
 - ISmimeCapability::get_ObjectId
 - certenroll/ISmimeCapability::get_ObjectId
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
 - ISmimeCapability.ObjectId
 - ISmimeCapability.get_ObjectId
---

# ISmimeCapability::get_ObjectId


## -description

The <b>ObjectId</b> property retrieves the object identifier (OID) of the symmetric encryption algorithm.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ismimecapability-initialize">Initialize</a> method to specify the <b>ObjectId</b> property. The following encryption OIDs are currently supported:

<ul>
<li>XCN_OID_NIST_AES128_CBC (2.16.840.1.101.3.4.1.2)</li>
<li>XCN_OID_NIST_AES192_CBC (2.16.840.1.101.3.4.1.22)</li>
<li>XCN_OID_NIST_AES256_CBC (2.16.840.1.101.3.4.1.42)</li>
<li>XCN_OID_NIST_AES128_WRAP (2.16.840.1.101.3.4.1.5)</li>
<li>XCN_OID_NIST_AES192_WRAP (2.16.840.1.101.3.4.1.25)</li>
<li>XCN_OID_NIST_AES256_WRAP (2.16.840.1.101.3.4.1.45)</li>
<li>XCN_OID_OIWSEC_desCBC (1.3.14.3.2.7)</li>
<li>XCN_OID_RSA_DES_EDE3_CBC (1.2.840.113549.3.7)</li>
<li>XCN_OID_RSA_RC2CBC (1.2.840.113549.3.2)</li>
<li>XCN_OID_RSA_RC4 (1.2.840.113549.3.4)</li>
<li>XCN_OID_RSA_SMIMEalgCMS3DESwrap (1.2.840.113549.1.9.16.3.6)</li>
<li>XCN_OID_RSA_SMIMEalgCMSRC2wrap (1.2.840.113549.1.9.16.3.7)</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapabilities">ISmimeCapabilities</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsmimecapabilities">IX509ExtensionSmimeCapabilities</a>