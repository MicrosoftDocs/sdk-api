---
UID: NN:certenroll.ICertPropertyEnrollmentPolicyServer
title: ICertPropertyEnrollmentPolicyServer
author: windows-sdk-content
description: Represents an external certificate property that contains information about a certificate enrollment policy (CEP) server and a certificate enrollment server (CES).
old-location: security\icertpropertyenrollmentpolicyserver.htm
tech.root: SecCertEnroll
ms.assetid: 1af7b178-3226-43c3-bfbe-08738f9ef851
ms.author: windowssdkdev
ms.date: 09/26/2018
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
</ul>In addition to the preceding policy information, a CEP web service also queries Active Directory for collections of available certification authorities, certificate templates, and custom object identifiers. These collections can be retrieved by using the <a href="https://msdn.microsoft.com/en-us/library/Ee351692(v=VS.85).aspx">IX509EnrollmentPolicyServer</a> interface.
<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/en-us/library/Aa374867(v=VS.85).aspx">CERTENROLL_PROPERTYID</a> value is XCN_CERT_CEP_PROP_ID.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyEnrollmentPolicyServer</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>. <b>ICertPropertyEnrollmentPolicyServer</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Ee338626(v=VS.85).aspx">GetAuthentication</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies the type of authentication used by the CEP server to authenticate a client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee338628(v=VS.85).aspx">GetEnrollmentServerAuthentication</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies the type of authentication used by the CES to authenticate a client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee338631(v=VS.85).aspx">GetEnrollmentServerUrl</a>
</td>
<td align="left" width="63%">
Retrieves a string that contains the URL for the certificate enrollment server (CES).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee338633(v=VS.85).aspx">GetPolicyServerId</a>
</td>
<td align="left" width="63%">
Retrieves a string that uniquely identifies the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee338635(v=VS.85).aspx">GetPolicyServerUrl</a>
</td>
<td align="left" width="63%">
Retrieves a string that contains the URL for the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee338637(v=VS.85).aspx">GetPropertyFlags</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies the default policy server URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee338639(v=VS.85).aspx">GetRequestIdString</a>
</td>
<td align="left" width="63%">
Retrieves a unique string identifier for the certificate request sent to the certification authority during enrollment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee338640(v=VS.85).aspx">GetUrlFlags</a>
</td>
<td align="left" width="63%">
Retrieves a set of flags that contain miscellaneous policy information about the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351591(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>ICertPropertyEnrollmentPolicyServer</b> object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee351692(v=VS.85).aspx">IX509EnrollmentPolicyServer</a>
 

 

