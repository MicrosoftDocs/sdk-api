---
UID: NN:certenroll.IX509Enrollment
title: IX509Enrollment
author: windows-sdk-content
description: Represents the top level object and enables you to enroll in a certificate hierarchy and install a certificate response.
old-location: security\ix509enrollment.htm
tech.root: seccertenroll
ms.assetid: 37f1dd3b-bbe9-40ab-87c9-2405d97f5541
ms.author: windowssdkdev
ms.date: 08/31/2018
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
 - IX509Enrollment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Enrollment interface


## -description


The <b>IX509Enrollment</b> interface represents the top level object and enables you to enroll in a certificate hierarchy and install a certificate response. The enrollment process supports the following three scenarios:<dl>
<dd>
Out-of-band enrollment

<ol>
<li>Call any initialization method implemented by the <b>IX509Enrollment</b> object.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377869(v=VS.85).aspx">CreateRequest</a> method.</li>
<li>Submit the request out of band (manually or through some other process).</li>
<li>Receive the response from a certification or registration authority.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378051(v=VS.85).aspx">InstallResponse</a> method.</li>
</ol>
</dd>
<dd>Automatic enrollment<ol>
<li>Call any initialization method implemented by the <b>IX509Enrollment</b> object.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377871(v=VS.85).aspx">Enroll</a> method.</li>
</ol>
</dd>
<dd>Delayed enrollment<ol>
<li>Call any initialization method implemented by the <b>IX509Enrollment</b> object.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377869(v=VS.85).aspx">CreateRequest</a> method.</li>
<li>Store the request for a period of time such as days or weeks.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378046(v=VS.85).aspx">Initialize</a> method to create a request object when you are ready to enroll.</li>
<li>Populate the request object from your stored request.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378051(v=VS.85).aspx">InstallResponse</a> method.</li>
</ol>
</dd>
</dl>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Enrollment</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509Enrollment</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377868(v=VS.85).aspx">CreatePFX</a>
</td>
<td align="left" width="63%">
Creates a Personal Information Exchange (PFX) message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377869(v=VS.85).aspx">CreateRequest</a>
</td>
<td align="left" width="63%">
Retrieves an encoded certificate request.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377871(v=VS.85).aspx">Enroll</a>
</td>
<td align="left" width="63%">
Encodes a request, submits it to an appropriate certification authority (CA), and installs the response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378046(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the enrollment object and creates a default PKCS #10 request.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377872(v=VS.85).aspx">InitializeFromRequest</a>
</td>
<td align="left" width="63%">
Initializes the enrollment object from an existing <a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a> object.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378023(v=VS.85).aspx">InitializeFromTemplateName</a>
</td>
<td align="left" width="63%">
Initializes the enrollment object from a template common name (CN).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378051(v=VS.85).aspx">InstallResponse</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa377864(v=VS.85).aspx">CAConfigString</a>


</td>
<td align="left" width="63%">
Retrieves the configuration string that identifies the certification authority (CA) to which the certificate request was submitted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377867(v=VS.85).aspx">Certificate</a>


</td>
<td align="left" width="63%">
Retrieves the installed certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377865(v=VS.85).aspx">CertificateDescription</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a string that contains a description of the certificate.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377866(v=VS.85).aspx">CertificateFriendlyName</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the display name of a certificate.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377870(v=VS.85).aspx">EnrollmentContext</a>


</td>
<td align="left" width="63%">
Retrieves an enrollment context that identifies whether the certificate is intended for a computer or an end user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378056(v=VS.85).aspx">NameValuePairs</a>


</td>
<td align="left" width="63%">
Retrieves a collection of name-value pairs associated with the enrollment object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378060(v=VS.85).aspx">ParentWindow</a>


</td>
<td align="left" width="63%">
Specifies or retrieves  the ID of the window used to display the enrollment information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378069(v=VS.85).aspx">Request</a>


</td>
<td align="left" width="63%">
Retrieves the certificate request associated with the enrollment object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378067(v=VS.85).aspx">RequestId</a>


</td>
<td align="left" width="63%">
Retrieves a unique identifier for the certificate request sent to the certification authority by the <a href="https://msdn.microsoft.com/en-us/library/Aa377871(v=VS.85).aspx">Enroll</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378071(v=VS.85).aspx">Response</a>


</td>
<td align="left" width="63%">
Retrieves the certificate response returned from a certification authority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378074(v=VS.85).aspx">Silent</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether a user interface is displayed during the certificate enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378076(v=VS.85).aspx">Status</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa377818(v=VS.85).aspx">IX509EnrollmentStatus</a> object that can be used to monitor the status of the enrollment process and retrieve error information.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374874(v=VS.85).aspx">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377818(v=VS.85).aspx">IX509EnrollmentStatus</a>
 

 

