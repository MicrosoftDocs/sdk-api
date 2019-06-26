---
UID: NN:certadm.ICertAdmin
title: ICertAdmin (certadm.h)
author: windows-sdk-content
description: Provides administration functionality for properly authorized clients.
old-location: security\icertadmin.htm
tech.root: SecCrypto
ms.assetid: e906b69b-5574-4dd5-aa30-9c2a67972202
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertAdmin, ICertAdmin interface [Security], ICertAdmin interface [Security],described, _certsrv_icertadmin, certadm/ICertAdmin, security.icertadmin
ms.topic: interface
f1_keywords: 
 - "certadm/ICertAdmin"
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertAdmin interface


## -description


The <b>ICertAdmin</b> interface
			provides administration functionality for properly authorized clients.

The <b>ICertAdmin</b> interface is used to perform the following tasks:
<ul>
<li>Authorize or deny a certificate request.</li>
<li>Revoke an issued certificate.</li>
<li>Trigger the generation of a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).</li>
<li>Get the current CRL for the server.</li>
<li>Determine whether a certificate is valid.</li>
</ul>When you use the <b>ICertAdmin</b> interface, you have write-only access to request attributes and certificate extensions, but no direct access to other request and certificate properties.

<b>ICertAdmin</b> is defined in Certadm.h. When you create a program, however, use Certsrv.h as the include file. Certadm.dll, on the other hand, provides the implementation of the <b>ICertAdmin</b> interface. The type information for this interface is also in Certadml.dll, which is shipped with the Platform Software Development Kit (SDK).

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertAdmin</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertAdmin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertAdmin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-denyrequest">DenyRequest</a>
</td>
<td align="left" width="63%">
Denies a certificate request.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-getcrl">GetCRL</a>
</td>
<td align="left" width="63%">
Gets a pointer to the current CRL.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-getrevocationreason">GetRevocationReason</a>
</td>
<td align="left" width="63%">
Returns a value that specifies the reason a certificate was revoked.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-importcertificate">ImportCertificate</a>
</td>
<td align="left" width="63%">
Imports a previously issued certificate.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-isvalidcertificate">IsValidCertificate</a>
</td>
<td align="left" width="63%">
Checks the validity of a certificate.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-publishcrl">PublishCRL</a>
</td>
<td align="left" width="63%">
Publishes a new CRL.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-resubmitrequest">ResubmitRequest</a>
</td>
<td align="left" width="63%">
Submits a pended certificate request to the policy module.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-revokecertificate">RevokeCertificate</a>
</td>
<td align="left" width="63%">
Revokes a certificate on a specified date.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-setcertificateextension">SetCertificateExtension</a>
</td>
<td align="left" width="63%">
Adds a new extension to a certificate to be issued.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-setrequestattributes">SetRequestAttributes</a>
</td>
<td align="left" width="63%">
Sets the attributes of a certificate request.</p> (Inherited from <b>ICertAdmin</b><b>CCertAdmin</b>)</td>
</tr>
</table> 

