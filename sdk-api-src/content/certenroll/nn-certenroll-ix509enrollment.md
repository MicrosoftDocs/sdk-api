---
UID: NN:certenroll.IX509Enrollment
title: IX509Enrollment
author: windows-sdk-content
description: Represents the top level object and enables you to enroll in a certificate hierarchy and install a certificate response.
old-location: security\ix509enrollment.htm
old-project: SecCertEnroll
ms.assetid: 37f1dd3b-bbe9-40ab-87c9-2405d97f5541
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509Enrollment, IX509Enrollment interface [Security], IX509Enrollment interface [Security],described, certenroll/IX509Enrollment, security.ix509enrollment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509Enrollment
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509Enrollment interface


## -description


The <b>IX509Enrollment</b> interface represents the top level object and enables you to enroll in a certificate hierarchy and install a certificate response. The enrollment process supports the following three scenarios:<dl>
<dd>
Out-of-band enrollment

<ol>
<li>Call any initialization method implemented by the <b>IX509Enrollment</b> object.</li>
<li>Call the <a href="https://msdn.microsoft.com/bc01a648-04c7-411e-8f7a-80f19433a200">CreateRequest</a> method.</li>
<li>Submit the request out of band (manually or through some other process).</li>
<li>Receive the response from a certification or registration authority.</li>
<li>Call the <a href="https://msdn.microsoft.com/4ad33092-71c4-4ae1-a3a6-cef376d04c2d">InstallResponse</a> method.</li>
</ol>
</dd>
<dd>Automatic enrollment<ol>
<li>Call any initialization method implemented by the <b>IX509Enrollment</b> object.</li>
<li>Call the <a href="https://msdn.microsoft.com/63abecac-39f4-497a-8851-7a2260abc3dd">Enroll</a> method.</li>
</ol>
</dd>
<dd>Delayed enrollment<ol>
<li>Call any initialization method implemented by the <b>IX509Enrollment</b> object.</li>
<li>Call the <a href="https://msdn.microsoft.com/bc01a648-04c7-411e-8f7a-80f19433a200">CreateRequest</a> method.</li>
<li>Store the request for a period of time such as days or weeks.</li>
<li>Call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method to create a request object when you are ready to enroll.</li>
<li>Populate the request object from your stored request.</li>
<li>Call the <a href="https://msdn.microsoft.com/4ad33092-71c4-4ae1-a3a6-cef376d04c2d">InstallResponse</a> method.</li>
</ol>
</dd>
</dl>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Enrollment</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IX509Enrollment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509Enrollment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a51bea0-e7f8-4a4e-b612-95616b126466">CreatePFX</a>
</td>
<td align="left" width="63%">
Creates a Personal Information Exchange (PFX) message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc01a648-04c7-411e-8f7a-80f19433a200">CreateRequest</a>
</td>
<td align="left" width="63%">
Retrieves an encoded certificate request.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63abecac-39f4-497a-8851-7a2260abc3dd">Enroll</a>
</td>
<td align="left" width="63%">
Encodes a request, submits it to an appropriate certification authority (CA), and installs the response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the enrollment object and creates a default PKCS #10 request.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04cb00af-f786-4548-bee3-2cc5083278c3">InitializeFromRequest</a>
</td>
<td align="left" width="63%">
Initializes the enrollment object from an existing <a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a> object.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44a934f4-9ae9-4f52-9d44-f5fcf30f3837">InitializeFromTemplateName</a>
</td>
<td align="left" width="63%">
Initializes the enrollment object from a template common name (CN).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ad33092-71c4-4ae1-a3a6-cef376d04c2d">InstallResponse</a>
</td>
<td align="left" width="63%">
Installs a certificate chain on the end-entity computer.

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Enrollment</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4a4478c8-a665-4ee1-9f3a-cad259e1c9ce">CAConfigString</a>


</td>
<td align="left" width="63%">
Retrieves the configuration string that identifies the certification authority (CA) to which the certificate request was submitted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/636e4c6d-38b9-4a27-b640-4c071816ee97">Certificate</a>


</td>
<td align="left" width="63%">
Retrieves the installed certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5057770b-79b1-4c83-bf2e-bff1eb91aea0">CertificateDescription</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a string that contains a description of the certificate.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/35c3eea1-2a3a-4e13-9232-f40429669948">CertificateFriendlyName</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the display name of a certificate.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/48bfe2cd-1d17-42a9-8068-b635fd220911">EnrollmentContext</a>


</td>
<td align="left" width="63%">
Retrieves an enrollment context that identifies whether the certificate is intended for a computer or an end user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d682fb7c-de80-4285-baa2-f86c997f0987">NameValuePairs</a>


</td>
<td align="left" width="63%">
Retrieves a collection of name-value pairs associated with the enrollment object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/154a73ae-e007-437b-87c3-33c2abb27aa4">ParentWindow</a>


</td>
<td align="left" width="63%">
Specifies or retrieves  the ID of the window used to display the enrollment information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/ff554564">Request</a>


</td>
<td align="left" width="63%">
Retrieves the certificate request associated with the enrollment object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/64048d5d-36fd-4709-a924-7f84a2b2b97e">RequestId</a>


</td>
<td align="left" width="63%">
Retrieves a unique identifier for the certificate request sent to the certification authority by the <a href="https://msdn.microsoft.com/63abecac-39f4-497a-8851-7a2260abc3dd">Enroll</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4580d376-0dbb-4418-a542-b0a9710862c4">Response</a>


</td>
<td align="left" width="63%">
Retrieves the certificate response returned from a certification authority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bd1f1e73-0c49-4a2f-9b29-8520da8e1d4b">Silent</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether a user interface is displayed during the certificate enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> object that can be used to monitor the status of the enrollment process and retrieve error information.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae6ab5fc-598e-43b8-a260-2cd94dc2648f">Certificate Enrollment API</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a>
 

 

