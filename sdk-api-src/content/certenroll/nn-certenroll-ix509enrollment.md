---
UID: NN:certenroll.IX509Enrollment
title: IX509Enrollment (certenroll.h)
description: Represents the top level object and enables you to enroll in a certificate hierarchy and install a certificate response.
helpviewer_keywords: ["IX509Enrollment","IX509Enrollment interface [Security]","IX509Enrollment interface [Security]","described","certenroll/IX509Enrollment","security.ix509enrollment"]
old-location: security\ix509enrollment.htm
tech.root: security
ms.assetid: 37f1dd3b-bbe9-40ab-87c9-2405d97f5541
ms.date: 12/05/2018
ms.keywords: IX509Enrollment, IX509Enrollment interface [Security], IX509Enrollment interface [Security],described, certenroll/IX509Enrollment, security.ix509enrollment
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
 - IX509Enrollment
 - certenroll/IX509Enrollment
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
 - IX509Enrollment
---

# IX509Enrollment interface


## -description

The <b>IX509Enrollment</b> interface represents the top level object and enables you to enroll in a certificate hierarchy and install a certificate response. The enrollment process supports the following three scenarios:<dl>
<dd>
Out-of-band enrollment

<ol>
<li>Call any initialization method implemented by the <b>IX509Enrollment</b> object.</li>
<li>Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-createrequest">CreateRequest</a> method.</li>
<li>Submit the request out of band (manually or through some other process).</li>
<li>Receive the response from a certification or registration authority.</li>
<li>Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-installresponse">InstallResponse</a> method.</li>
</ol>
</dd>
<dd>Automatic enrollment<ol>
<li>Call any initialization method implemented by the <b>IX509Enrollment</b> object.</li>
<li>Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-enroll">Enroll</a> method.</li>
</ol>
</dd>
<dd>Delayed enrollment<ol>
<li>Call any initialization method implemented by the <b>IX509Enrollment</b> object.</li>
<li>Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-createrequest">CreateRequest</a> method.</li>
<li>Store the request for a period of time such as days or weeks.</li>
<li>Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initialize">Initialize</a> method to create a request object when you are ready to enroll.</li>
<li>Populate the request object from your stored request.</li>
<li>Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-installresponse">InstallResponse</a> method.</li>
</ol>
</dd>
</dl>

## -inheritance

The <b>IX509Enrollment</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509Enrollment</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a>
