---
UID: NN:certenroll.ICertPropertyEnrollmentPolicyServer
title: ICertPropertyEnrollmentPolicyServer (certenroll.h)
description: Represents an external certificate property that contains information about a certificate enrollment policy (CEP) server and a certificate enrollment server (CES).
helpviewer_keywords: ["ICertPropertyEnrollmentPolicyServer","ICertPropertyEnrollmentPolicyServer interface [Security]","ICertPropertyEnrollmentPolicyServer interface [Security]","described","certenroll/ICertPropertyEnrollmentPolicyServer","security.icertpropertyenrollmentpolicyserver"]
old-location: security\icertpropertyenrollmentpolicyserver.htm
tech.root: security
ms.assetid: 1af7b178-3226-43c3-bfbe-08738f9ef851
ms.date: 12/05/2018
ms.keywords: ICertPropertyEnrollmentPolicyServer, ICertPropertyEnrollmentPolicyServer interface [Security], ICertPropertyEnrollmentPolicyServer interface [Security],described, certenroll/ICertPropertyEnrollmentPolicyServer, security.icertpropertyenrollmentpolicyserver
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: CertEnroll.dll
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertPropertyEnrollmentPolicyServer
 - certenroll/ICertPropertyEnrollmentPolicyServer
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
 - ICertPropertyEnrollmentPolicyServer
---

# ICertPropertyEnrollmentPolicyServer interface


## -description

The <b>ICertPropertyEnrollmentPolicyServer</b> interface represents an external certificate property that contains information about a certificate enrollment policy (CEP) server and a certificate enrollment server (CES).  A CEP server is a web service that retrieves policy information. A CES is a web service that targets a specific certification authority to support certificate enrollment.

The following list identifies the policy data managed by this interface and which can be added as a property value to an issued certificate.
<ul>
<li>The CEP client authentication method.</li>
<li>The CES client authentication method.</li>
<li>The CEP URL.</li>
<li>The CES URL.</li>
<li>The CEP ID.</li>
<li>The request ID string.</li>
</ul>In addition to the preceding policy information, a CEP web service also queries Active Directory for collections of available certification authorities, certificate templates, and custom object identifiers. These collections can be retrieved by using the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a> interface.
<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_CEP_PROP_ID.</div><div> </div>

## -inheritance

The <b>ICertPropertyEnrollmentPolicyServer</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyEnrollmentPolicyServer</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>
