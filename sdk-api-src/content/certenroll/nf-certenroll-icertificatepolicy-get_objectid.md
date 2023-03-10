---
UID: NF:certenroll.ICertificatePolicy.get_ObjectId
title: ICertificatePolicy::get_ObjectId (certenroll.h)
description: Retrieves an object identifier (OID) for the policy object.
helpviewer_keywords: ["ICertificatePolicy interface [Security]","ObjectId property","ICertificatePolicy.ObjectId","ICertificatePolicy.get_ObjectId","ICertificatePolicy::ObjectId","ICertificatePolicy::get_ObjectId","ObjectId property [Security]","ObjectId property [Security]","ICertificatePolicy interface","certenroll/ICertificatePolicy::ObjectId","certenroll/ICertificatePolicy::get_ObjectId","get_ObjectId","security.icertificatepolicy_objectid_property"]
old-location: security\icertificatepolicy_objectid_property.htm
tech.root: security
ms.assetid: 42d1689d-c086-4d67-8e16-997ecd515ae2
ms.date: 12/05/2018
ms.keywords: ICertificatePolicy interface [Security],ObjectId property, ICertificatePolicy.ObjectId, ICertificatePolicy.get_ObjectId, ICertificatePolicy::ObjectId, ICertificatePolicy::get_ObjectId, ObjectId property [Security], ObjectId property [Security],ICertificatePolicy interface, certenroll/ICertificatePolicy::ObjectId, certenroll/ICertificatePolicy::get_ObjectId, get_ObjectId, security.icertificatepolicy_objectid_property
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
 - ICertificatePolicy::get_ObjectId
 - certenroll/ICertificatePolicy::get_ObjectId
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
 - ICertificatePolicy.ObjectId
 - ICertificatePolicy.get_ObjectId
---

# ICertificatePolicy::get_ObjectId


## -description

The <b>ObjectId</b> property retrieves an object identifier (OID) for the policy object.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> object stores information about the OID internally in a CryptoAPI <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info">CRYPT_OID_INFO</a> structure. You cannot use this structure directly from the  Certificate Enrollment API, but you can use the  <b>IObjectId</b> interface to retrieve the display name or dotted decimal name of the OID, or the <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a> value.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicies">ICertificatePolicies</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a>