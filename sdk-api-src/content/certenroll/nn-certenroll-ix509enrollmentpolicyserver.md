---
UID: NN:certenroll.IX509EnrollmentPolicyServer
title: IX509EnrollmentPolicyServer
author: windows-sdk-content
description: The IX509EnrollmentPolicyServer interface represents a certificate enrollment policy (CEP) server.
old-location: security\ix509enrollmentpolicyserver.htm
tech.root: seccertenroll
ms.assetid: e39d40fd-3d43-4cdc-b41a-07a87a11bfad
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509EnrollmentPolicyServer, IX509EnrollmentPolicyServer interface [Security], IX509EnrollmentPolicyServer interface [Security],described, certenroll/IX509EnrollmentPolicyServer, security.ix509enrollmentpolicyserver
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
 - IX509EnrollmentPolicyServer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509EnrollmentPolicyServer interface


## -description


The <b>IX509EnrollmentPolicyServer</b> interface represents a certificate enrollment policy (CEP) server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentPolicyServer</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509EnrollmentPolicyServer</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IX509EnrollmentPolicyServer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351694(v=VS.85).aspx">Export</a>
</td>
<td align="left" width="63%">
Exports templates and object identifiers associated with the CEP server to a buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351695(v=VS.85).aspx">GetAllowUnTrustedCA</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether to allow an untrusted certification authority certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351696(v=VS.85).aspx">GetAuthFlags</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies the authentication type used by the client to authenticate itself to the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351697(v=VS.85).aspx">GetCacheDir</a>
</td>
<td align="left" width="63%">
Retrieves the name of the directory on the CEP server that contains the policy cache file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351698(v=VS.85).aspx">GetCachePath</a>
</td>
<td align="left" width="63%">
Retrieves the path of the policy cache file on the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351699(v=VS.85).aspx">GetCAs</a>
</td>
<td align="left" width="63%">
Retrieves a collection of certification enrollment servers included in the policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351700(v=VS.85).aspx">GetCAsForTemplate</a>
</td>
<td align="left" width="63%">
Retrieves a collection of certificate enrollment servers that support a specified template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351701(v=VS.85).aspx">GetCustomOids</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351702(v=VS.85).aspx">GetFriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves a display name for the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351703(v=VS.85).aspx">GetIsDefaultCEP</a>
</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether this is the default CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351704(v=VS.85).aspx">GetLastUpdateTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time at which the policy was last downloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351705(v=VS.85).aspx">GetNextUpdateTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time at which the policy expires and should be refreshed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351706(v=VS.85).aspx">GetPolicyServerId</a>
</td>
<td align="left" width="63%">
Retrieves a string value that uniquely identifies the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351707(v=VS.85).aspx">GetPolicyServerUrl</a>
</td>
<td align="left" width="63%">
Retrieves a string value that contains the URL for the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351708(v=VS.85).aspx">GetTemplates</a>
</td>
<td align="left" width="63%">
Retrieves a collection of the templates supported by the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351709(v=VS.85).aspx">GetUseClientId</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether the <b>ClientId</b> attribute is set in the policy server flags of the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351710(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>IX509EnrollmentPolicyServer</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351711(v=VS.85).aspx">InitializeImport</a>
</td>
<td align="left" width="63%">
Initializes the CEP server from a collection of templates and object identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351712(v=VS.85).aspx">LoadPolicy</a>
</td>
<td align="left" width="63%">
Retrieves policy information from the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351713(v=VS.85).aspx">QueryChanges</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether the template or certification authority collections have changed in Active Directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351714(v=VS.85).aspx">SetCredential</a>
</td>
<td align="left" width="63%">
Sets the credential used to contact the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee351715(v=VS.85).aspx">Validate</a>
</td>
<td align="left" width="63%">
Validates the current policy information.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentPolicyServer</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Ee351693(v=VS.85).aspx">Cost</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies and retrieves an arbitrary  cost for contacting the certificate enrollment policy server.

</td>
</tr>
</table> 

