---
UID: NN:certenroll.IX509EnrollmentStatus
title: IX509EnrollmentStatus (certenroll.h)
author: windows-sdk-content
description: The IX509EnrollmentStatus interface can be used to specify or retrieve detailed error information about a certificate enrollment transaction.
old-location: security\ix509enrollmentstatus.htm
tech.root: seccertenroll
ms.assetid: fa5e3a10-7f00-46b6-b740-b72d78745bf7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509EnrollmentStatus, IX509EnrollmentStatus interface [Security], IX509EnrollmentStatus interface [Security],described, certenroll/IX509EnrollmentStatus, security.ix509enrollmentstatus
ms.topic: interface
f1_keywords: 
 - "certenroll/IX509EnrollmentStatus"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509EnrollmentStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509EnrollmentStatus interface


## -description


The <b>IX509EnrollmentStatus</b> interface can be used to specify or retrieve detailed error information about a certificate enrollment transaction.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentStatus</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509EnrollmentStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509EnrollmentStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-appendtext">AppendText</a>
</td>
<td align="left" width="63%">
Appends a string to the status information contained in the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_text">Text</a> property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentStatus</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_display">Display</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value that indicates whether to display the status information in a user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_error">Error</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a value that identifies the error status of the certificate enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_errortext">ErrorText</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains the message associated with the error result code returned by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_error">Error</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value that indicates whether an item can be used during the enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_status">Status</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value that indicates the status of the enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_text">Text</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a string that contains a message associated with the status of the enrollment process.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>
 

 

