---
UID: NN:certenroll.IX509Enrollment2
title: IX509Enrollment2
author: windows-sdk-content
description: The IX509Enrollment2 interface enables you to enroll in a certificate hierarchy and install a certificate response.
old-location: security\ix509enrollment2.htm
tech.root: SecCertEnroll
ms.assetid: 8e262b4b-de6a-417e-9ade-0b451bd4c09a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509Enrollment2, IX509Enrollment2 interface [Security], IX509Enrollment2 interface [Security],described, certenroll/IX509Enrollment2, security.ix509enrollment2
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
 - IX509Enrollment2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Enrollment2 interface


## -description


The <b>IX509Enrollment2</b> interface enables you to enroll in a certificate hierarchy and install a certificate response. It includes all of the methods defined by the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> interface and adds methods that enable initialization from certificate request templates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Enrollment2</b> interface inherits from <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>. <b>IX509Enrollment2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509Enrollment2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa260ff7-d55b-4fda-88e2-2f1d68cc41e1">InitializeFromTemplate</a>
</td>
<td align="left" width="63%">
Initializes the enrollment object by using a template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a5dce88-afc5-4d47-85e8-980192a662d8">InstallResponse2</a>
</td>
<td align="left" width="63%">
Installs a certificate chain on the end-entity computer.

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Enrollment2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dae8489b-39b1-41ba-9346-c038cd0acc1b">PolicyServer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the certificate enrollment policy (CEP) server that contains the template used during initialization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a1269b0d-6b55-47ba-bca8-610c1032ecc4">RequestIdString</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a string that contains a unique identifier for the certificate request sent to the certification enrollment server (CES).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/14b6fab5-36d1-490b-9416-ff77f6bb7e01">Template</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the certificate request template used during initialization.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>
 

 

