---
UID: NN:certenroll.IX509EnrollmentHelper
title: IX509EnrollmentHelper
author: windows-sdk-content
description: The IX509EnrollmentHelper interface defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.
old-location: security\ix509enrollmenthelper.htm
tech.root: seccertenroll
ms.assetid: 19124591-be1a-401e-9b83-c640d00de34a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509EnrollmentHelper, IX509EnrollmentHelper interface [Security], IX509EnrollmentHelper interface [Security],described, certenroll/IX509EnrollmentHelper, security.ix509enrollmenthelper
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509EnrollmentHelper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509EnrollmentHelper interface


## -description


The <b>IX509EnrollmentHelper</b> interface defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentHelper</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IX509EnrollmentHelper</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a354fc02-299d-472c-9821-1509e299ccb9">AddEnrollmentServer</a>
</td>
<td align="left" width="63%">
Saves certificate enrollment server (CES) access credentials in the credential cache.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b341b5a-88f2-4221-812d-b2997829aa4c">AddPolicyServer</a>
</td>
<td align="left" width="63%">
Registers a certificate enrollment policy (CEP) server and saves CEP access credentials in the credential cache.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f178df7-714f-49e6-9bf5-647acc23b0ad">Enroll</a>
</td>
<td align="left" width="63%">
Enrolls a certificate request and retrieves the issued certificate.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83cb603b-9396-4983-8707-12d1c5b8b234">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>IX509EnrollmentHelper</b> object.

</td>
</tr>
</table> 

