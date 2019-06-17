---
UID: NN:certenroll.IX509EnrollmentPolicyServer
title: IX509EnrollmentPolicyServer (certenroll.h)
author: windows-sdk-content
description: The IX509EnrollmentPolicyServer interface represents a certificate enrollment policy (CEP) server.
old-location: security\ix509enrollmentpolicyserver.htm
tech.root: seccertenroll
ms.assetid: e39d40fd-3d43-4cdc-b41a-07a87a11bfad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509EnrollmentPolicyServer, IX509EnrollmentPolicyServer interface [Security], IX509EnrollmentPolicyServer interface [Security],described, certenroll/IX509EnrollmentPolicyServer, security.ix509enrollmentpolicyserver
ms.topic: interface
f1_keywords: ["certenroll/IX509EnrollmentPolicyServer"]
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
ms.custom: 19H1
---

# IX509EnrollmentPolicyServer interface


## -description


The <b>IX509EnrollmentPolicyServer</b> interface represents a certificate enrollment policy (CEP) server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentPolicyServer</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509EnrollmentPolicyServer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-export">Export</a>
</td>
<td align="left" width="63%">
Exports templates and object identifiers associated with the CEP server to a buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getallowuntrustedca">GetAllowUnTrustedCA</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether to allow an untrusted certification authority certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getauthflags">GetAuthFlags</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies the authentication type used by the client to authenticate itself to the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getcachedir">GetCacheDir</a>
</td>
<td align="left" width="63%">
Retrieves the name of the directory on the CEP server that contains the policy cache file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getcachepath">GetCachePath</a>
</td>
<td align="left" width="63%">
Retrieves the path of the policy cache file on the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getcas">GetCAs</a>
</td>
<td align="left" width="63%">
Retrieves a collection of certification enrollment servers included in the policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getcasfortemplate">GetCAsForTemplate</a>
</td>
<td align="left" width="63%">
Retrieves a collection of certificate enrollment servers that support a specified template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getcustomoids">GetCustomOids</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getfriendlyname">GetFriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves a display name for the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getisdefaultcep">GetIsDefaultCEP</a>
</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether this is the default CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getlastupdatetime">GetLastUpdateTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time at which the policy was last downloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getnextupdatetime">GetNextUpdateTime</a>
</td>
<td align="left" width="63%">
Retrieves the date and time at which the policy expires and should be refreshed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getpolicyserverid">GetPolicyServerId</a>
</td>
<td align="left" width="63%">
Retrieves a string value that uniquely identifies the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getpolicyserverurl">GetPolicyServerUrl</a>
</td>
<td align="left" width="63%">
Retrieves a string value that contains the URL for the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-gettemplates">GetTemplates</a>
</td>
<td align="left" width="63%">
Retrieves a collection of the templates supported by the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getuseclientid">GetUseClientId</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether the <b>ClientId</b> attribute is set in the policy server flags of the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>IX509EnrollmentPolicyServer</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-initializeimport">InitializeImport</a>
</td>
<td align="left" width="63%">
Initializes the CEP server from a collection of templates and object identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-loadpolicy">LoadPolicy</a>
</td>
<td align="left" width="63%">
Retrieves policy information from the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-querychanges">QueryChanges</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies whether the template or certification authority collections have changed in Active Directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-setcredential">SetCredential</a>
</td>
<td align="left" width="63%">
Sets the credential used to contact the CEP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-validate">Validate</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-get_cost">Cost</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies and retrieves an arbitrary  cost for contacting the certificate enrollment policy server.

</td>
</tr>
</table> 

