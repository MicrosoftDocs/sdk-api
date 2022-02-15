---
UID: NN:casetup.ICertificateEnrollmentPolicyServerSetup
title: ICertificateEnrollmentPolicyServerSetup (casetup.h)
description: The ICertificateEnrollmentPolicyServerSetup interface represents the Certificate Enrollment Policy (CEP) Web Service within Active Directory Certificate Services (ADCS).
helpviewer_keywords: ["ICertificateEnrollmentPolicyServerSetup","ICertificateEnrollmentPolicyServerSetup interface [Security]","ICertificateEnrollmentPolicyServerSetup interface [Security]","described","casetup/ICertificateEnrollmentPolicyServerSetup","security.icertificateenrollmentpolicyserversetup"]
old-location: security\icertificateenrollmentpolicyserversetup.htm
tech.root: security
ms.assetid: 8C9F33BA-5FCB-4B99-869C-FADDC37A326A
ms.date: 12/05/2018
ms.keywords: ICertificateEnrollmentPolicyServerSetup, ICertificateEnrollmentPolicyServerSetup interface [Security], ICertificateEnrollmentPolicyServerSetup interface [Security],described, casetup/ICertificateEnrollmentPolicyServerSetup, security.icertificateenrollmentpolicyserversetup
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertificateEnrollmentPolicyServerSetup
 - casetup/ICertificateEnrollmentPolicyServerSetup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertificateEnrollmentPolicyServerSetup
---

# ICertificateEnrollmentPolicyServerSetup interface


## -description

The <b>ICertificateEnrollmentPolicyServerSetup</b> interface represents the Certificate Enrollment Policy (CEP) Web Service within Active Directory Certificate Services (ADCS). The service enables users and computers to obtain certificate enrollment policy information even when a  computer is not a member of the domain or if a domain-joined computer is temporarily outside the security boundary of the corporate network.

A related interface, <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a>, represents the Certificate Enrollment Web Service (CES) and enables users and computers to enroll for and renew certificates. CEP and CES work together to provide policy-based certificate enrollment.

## -inheritance

The <b>ICertificateEnrollmentPolicyServerSetup</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertificateEnrollmentPolicyServerSetup</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
