---
UID: NN:certenroll.ICertPropertyArchived
title: ICertPropertyArchived (certenroll.h)
description: Represents a certificate property that identifies whether a certificate has been archived.
helpviewer_keywords: ["ICertPropertyArchived","ICertPropertyArchived interface [Security]","ICertPropertyArchived interface [Security]","described","certenroll/ICertPropertyArchived","security.icertpropertyarchived"]
old-location: security\icertpropertyarchived.htm
tech.root: security
ms.assetid: 81219ad9-4717-40e5-9ecd-d3df980e23c6
ms.date: 12/05/2018
ms.keywords: ICertPropertyArchived, ICertPropertyArchived interface [Security], ICertPropertyArchived interface [Security],described, certenroll/ICertPropertyArchived, security.icertpropertyarchived
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
 - ICertPropertyArchived
 - certenroll/ICertPropertyArchived
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
 - ICertPropertyArchived
---

# ICertPropertyArchived interface


## -description

The <b>ICertPropertyArchived</b> interface represents a certificate property that identifies whether a certificate has been archived. Typically, a certificate is archived after being renewed, and this property is set so that archived certificates can be identified and skipped during enumeration.

This property is initialized by the enrollment process after the client requests that a certificate be renewed. If a new certificate is issued, the property is associated with the old certificate in the personal store.<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_ARCHIVED_PROP_ID.</div>
<div> </div>

## -inheritance

The <b>ICertPropertyArchived</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyArchived</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>
