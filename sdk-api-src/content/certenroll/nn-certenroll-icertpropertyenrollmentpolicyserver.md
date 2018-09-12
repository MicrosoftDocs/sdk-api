---
UID: NN:certenroll.ICertPropertyEnrollmentPolicyServer
title: ICertPropertyEnrollmentPolicyServer
author: windows-sdk-content
description: Represents an external certificate property that contains information about a certificate enrollment policy (CEP) server and a certificate enrollment server (CES).
old-location: security\icertpropertyenrollmentpolicyserver.htm
tech.root: SecCertEnroll
ms.assetid: 1af7b178-3226-43c3-bfbe-08738f9ef851
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICertPropertyEnrollmentPolicyServer, ICertPropertyEnrollmentPolicyServer interface [Security], ICertPropertyEnrollmentPolicyServer interface [Security],described, certenroll/ICertPropertyEnrollmentPolicyServer, security.icertpropertyenrollmentpolicyserver
ms.prod: windows
ms.technology: windows-sdk
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
 - ICertPropertyEnrollmentPolicyServer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyEnrollmentPolicyServer interface


## -description


The <b>ICertPropertyEnrollmentPolicyServer</b> interface represents an external certificate property that contains information about a certificate enrollment policy (CEP) server and a certificate enrollment server (CES).  A CEP server is a web service that retrieves policy information. A CES is a web service that targets a specific certification authority to support certificate enrollment.

The following list identifies the policy data managed by this interface and which can be added as a property value to an issued certificate.
<ul>
<li>The CEP client authentication method.</li>
<li>The CES client authentication method.</li>
<li>The CEP URL.</li>
<li>The CES URL</li>
<li>The CEP ID.</li>
<li>The request ID string.</li>
</ul>In addition to the preceding policy information, a CEP web service also queries Active Directory for collections of available certification authorities, certificate templates, and custom object identifiers. These collections can be retrieved by using the <a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a> interface.
<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/e7ad0ec5-a568-4506-ba54-908e00083c2b">CERTENROLL_PROPERTYID</a> value is XCN_CERT_CEP_PROP_ID.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyEnrollmentPolicyServer</b> interface inherits from <a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>. <b>ICertPropertyEnrollmentPolicyServer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertPropertyEnrollmentPolicyServer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56f6e7b8-4ed2-47fe-bc57-e238668c5264">GetAuthentication</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies the type of authentication used by the CEP server to authenticate a client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c46d9bc4-26ee-40c0-a228-804e7c598285">GetEnrollmentServerAuthentication</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies the type of authentication used by the CES to authenticate a client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d8e7f45-f7ff-48d0-95d8-4d426e122554">GetEnrollmentServerUrl</a>
</td>
<td align="left" width="63%">
Retrieves a string that contains the URL for the certificate enrollment server (CES).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0cd9f41-d697-4c27-9aff-a37de62d1bad">GetPolicyServerId</a>
</td>
<td align="left" width="63%">
Retrieves a string that uniquely identifies the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d7ba049-4566-423d-b750-ff091dce1e2a">GetPolicyServerUrl</a>
</td>
<td align="left" width="63%">
Retrieves a string that contains the URL for the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80d1af3c-2d1a-4d19-aed6-8cb2d3e52535">GetPropertyFlags</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies the default policy server URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9855a9d-938f-4579-8447-a931dbba1428">GetRequestIdString</a>
</td>
<td align="left" width="63%">
Retrieves a unique string identifier for the certificate request sent to the certification authority during enrollment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eafd4290-5eef-432f-908c-0640a4ac667f">GetUrlFlags</a>
</td>
<td align="left" width="63%">
Retrieves a set of flags that contain miscellaneous policy information about the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d54ffb2-4a81-4d52-80db-b8526a52bb53">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>ICertPropertyEnrollmentPolicyServer</b> object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>



<a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a>
 

 

