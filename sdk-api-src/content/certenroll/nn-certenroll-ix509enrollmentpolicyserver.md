---
UID: NN:certenroll.IX509EnrollmentPolicyServer
title: IX509EnrollmentPolicyServer
author: windows-sdk-content
description: The IX509EnrollmentPolicyServer interface represents a certificate enrollment policy (CEP) server.
old-location: security\ix509enrollmentpolicyserver.htm
old-project: SecCertEnroll
ms.assetid: e39d40fd-3d43-4cdc-b41a-07a87a11bfad
ms.author: windowssdkdev
ms.date: 05/10/2018
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
 - IX509EnrollmentPolicyServer
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509EnrollmentPolicyServer interface


## -description


The <b>IX509EnrollmentPolicyServer</b> interface represents a certificate enrollment policy (CEP) server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentPolicyServer</b> interface inherits from the <a href="http://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IX509EnrollmentPolicyServer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
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
<a href="https://msdn.microsoft.com/b821329b-2ec6-4f47-ba5f-2e1cd7ffb06f">Export</a>
</td>
<td align="left" width="63%">
Exports templates and object identifiers associated with the CEP server to a buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b15a2ba-2e68-4c66-910d-20dd0f0581c2">GetAllowUnTrustedCA</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether to allow an untrusted certification authority certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29ecfb93-82ec-4d34-84ea-0a181e134b6a">GetAuthFlags</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies the authentication type used by the client to authenticate itself to the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72b0b6f0-cc4f-4e03-9b6c-7bd4c12cf0a3">GetCacheDir</a>
</td>
<td align="left" width="63%">
Retrieves the name of the directory on the CEP server that contains the policy cache file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c71c9f97-a312-4260-995b-454de6a38cce">GetCachePath</a>
</td>
<td align="left" width="63%">
Retrieves the path of the policy cache file on the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37836fd1-e95a-4025-b268-f78a9113e568">GetCAs</a>
</td>
<td align="left" width="63%">
Retrieves a collection of certification enrollment servers included in the policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7330aea0-36b3-49fa-8970-2476f2ae9d34">GetCAsForTemplate</a>
</td>
<td align="left" width="63%">
Retrieves a collection of certificate enrollment servers that support a specified template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0db4e188-cef1-46af-b5c7-f18a8de5f1a7">GetCustomOids</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406579">GetFriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves a display name for the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c84993b-5d08-45c1-8139-458b047028aa">GetIsDefaultCEP</a>
</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether this is the default CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f0ec30a-9a93-47f9-8046-8eba6eb3b1da">GetLastUpdateTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time at which the policy was last downloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23ddd933-2392-410b-a4e6-7f5c00f867b3">GetNextUpdateTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time at which the policy expires and should be refreshed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/daff74e8-a124-4194-95f6-5837598c352f">GetPolicyServerId</a>
</td>
<td align="left" width="63%">
Retrieves a string value that uniquely identifies the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34fb1430-afde-43f2-a425-dcb25c9ea58d">GetPolicyServerUrl</a>
</td>
<td align="left" width="63%">
Retrieves a string value that contains the URL for the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52dd85aa-033b-43ab-9b71-1080f969bebc">GetTemplates</a>
</td>
<td align="left" width="63%">
Retrieves a collection of the templates supported by the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fd74752-60bb-4bdb-973d-76d4ab0ae4c4">GetUseClientId</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether the <b>ClientId</b> attribute is set in the policy server flags of the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>IX509EnrollmentPolicyServer</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b397f57f-e01e-4c2b-8338-892f56b76c9e">InitializeImport</a>
</td>
<td align="left" width="63%">
Initializes the CEP server from a collection of templates and object identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b617c6e-91bc-4a22-acd6-41083102850a">LoadPolicy</a>
</td>
<td align="left" width="63%">
Retrieves policy information from the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c83faaba-0355-4765-bc08-5e0e02afe8c2">QueryChanges</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether the template or certification authority collections have changed in Active Directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64ea6d9e-8eca-4a1b-95a0-ecc5c0d37df3">SetCredential</a>
</td>
<td align="left" width="63%">
Sets the credential used to contact the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab58622e-79a6-4a1b-a0e2-74efb81c7062">Validate</a>
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

<a href="https://msdn.microsoft.com/e79bc71f-5f7b-47d7-b45b-1279d27439d2">Cost</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies and retrieves an arbitrary  cost for contacting the certificate enrollment policy server.

</td>
</tr>
</table> 

