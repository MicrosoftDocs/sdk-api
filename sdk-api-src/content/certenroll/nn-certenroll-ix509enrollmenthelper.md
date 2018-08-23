---
UID: NN:certenroll.IX509EnrollmentHelper
title: IX509EnrollmentHelper
author: windows-sdk-content
description: The IX509EnrollmentHelper interface defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.
old-location: security\ix509enrollmenthelper.htm
old-project: seccertenroll
ms.assetid: 19124591-be1a-401e-9b83-c640d00de34a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509EnrollmentHelper, IX509EnrollmentHelper interface [Security], IX509EnrollmentHelper interface [Security],described, certenroll/IX509EnrollmentHelper, security.ix509enrollmenthelper
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509EnrollmentHelper interface


## -description


The <b>IX509EnrollmentHelper</b> interface defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentHelper</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509EnrollmentHelper</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Ee351688(v=VS.85).aspx">AddEnrollmentServer</a>
</td>
<td align="left" width="63%">
Saves certificate enrollment server (CES) access credentials in the credential cache.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351689(v=VS.85).aspx">AddPolicyServer</a>
</td>
<td align="left" width="63%">
Registers a certificate enrollment policy (CEP) server and saves CEP access credentials in the credential cache.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351690(v=VS.85).aspx">Enroll</a>
</td>
<td align="left" width="63%">
Enrolls a certificate request and retrieves the issued certificate.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351691(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>IX509EnrollmentHelper</b> object.

</td>
</tr>
</table> 

