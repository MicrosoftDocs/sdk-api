---
UID: NN:certenroll.IX509EnrollmentHelper
title: IX509EnrollmentHelper (certenroll.h)
description: The IX509EnrollmentHelper interface defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.
helpviewer_keywords: ["IX509EnrollmentHelper","IX509EnrollmentHelper interface [Security]","IX509EnrollmentHelper interface [Security]","described","certenroll/IX509EnrollmentHelper","security.ix509enrollmenthelper"]
old-location: security\ix509enrollmenthelper.htm
tech.root: security
ms.assetid: 19124591-be1a-401e-9b83-c640d00de34a
ms.date: 12/05/2018
ms.keywords: IX509EnrollmentHelper, IX509EnrollmentHelper interface [Security], IX509EnrollmentHelper interface [Security],described, certenroll/IX509EnrollmentHelper, security.ix509enrollmenthelper
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
 - IX509EnrollmentHelper
 - certenroll/IX509EnrollmentHelper
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
 - IX509EnrollmentHelper
---

# IX509EnrollmentHelper interface


## -description

The <b>IX509EnrollmentHelper</b> interface defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentHelper</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509EnrollmentHelper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IX509EnrollmentHelper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmenthelper-addenrollmentserver">AddEnrollmentServer</a>
</td>
<td align="left" width="63%">
Saves certificate enrollment server (CES) access credentials in the credential cache.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmenthelper-addpolicyserver">AddPolicyServer</a>
</td>
<td align="left" width="63%">
Registers a certificate enrollment policy (CEP) server and saves CEP access credentials in the credential cache.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmenthelper-enroll">Enroll</a>
</td>
<td align="left" width="63%">
Enrolls a certificate request and retrieves the issued certificate.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmenthelper-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>IX509EnrollmentHelper</b> object.

</td>
</tr>
</table>