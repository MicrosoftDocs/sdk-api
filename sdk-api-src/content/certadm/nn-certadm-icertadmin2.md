---
UID: NN:certadm.ICertAdmin2
title: ICertAdmin2 (certadm.h)
author: windows-sdk-content
description: Provide administration functionality for properly authorized clients.
old-location: security\icertadmin2.htm
tech.root: SecCrypto
ms.assetid: df40b6ac-825d-4e8d-a80b-6e57a4e740a2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertAdmin2, ICertAdmin2 interface [Security], ICertAdmin2 interface [Security],described, _certsrv_icertadmin2, certadm/ICertAdmin2, security.icertadmin2
ms.topic: interface
f1_keywords: ["certadm/ICertAdmin2"]
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
 - ICertAdmin2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertAdmin2 interface


## -description


The <b>ICertAdmin2</b> interface
			is one of two interfaces that provide administration functionality for properly authorized clients.

The <b>ICertAdmin2</b> interface is used to perform the following tasks:
<ul>
<li>Authorize or deny a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a>.</li>
<li>Revoke an issued certificate.</li>
<li>Trigger the generation of a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).</li>
<li>Get the current CRL for the server.</li>
<li>Determine whether a certificate is valid.</li>
<li>Get an archived key.</li>
<li>Get a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) display name, property, or property flag.</li>
<li>Publish one or several CRLs.</li>
<li>Get or set configuration information.</li>
<li>Determine which roles are set.</li>
<li>Import a certificate or key.</li>
</ul>Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertAdmin2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. <b>ICertAdmin2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertAdmin2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-deleterow">DeleteRow</a>
</td>
<td align="left" width="63%">
Deletes a row, or set of rows, from a database table.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-denyrequest">DenyRequest</a>
</td>
<td align="left" width="63%">
Denies a certificate request.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-getarchivedkey">GetArchivedKey</a>
</td>
<td align="left" width="63%">
Retrieves an archived key recovery <a href="https://docs.microsoft.com/windows/desktop/SecGloss/b-gly">BLOB</a>.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcaproperty">GetCAProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcapropertydisplayname">GetCAPropertyDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for a property.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcapropertyflags">GetCAPropertyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the property flags (denoting data type and indexed status) for a property.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-getconfigentry">GetConfigEntry</a>
</td>
<td align="left" width="63%">
Retrieves configuration  information for a CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-getcrl">GetCRL</a>
</td>
<td align="left" width="63%">
Gets a pointer to the current CRL.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-getmyroles">GetMyRoles</a>
</td>
<td align="left" width="63%">
Retrieves the CA roles of the caller.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-getrevocationreason">GetRevocationReason</a>
</td>
<td align="left" width="63%">
Returns a value that specifies the reason a certificate was revoked.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-importcertificate">ImportCertificate</a>
</td>
<td align="left" width="63%">
Imports a previously issued certificate.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-importkey">ImportKey</a>
</td>
<td align="left" width="63%">
Adds an encrypted key set to an item in the Certificate Services database. The  key set is encrypted to one or several key recovery agent (KRA) certificates.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-isvalidcertificate">IsValidCertificate</a>
</td>
<td align="left" width="63%">
Checks the validity of a certificate.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-publishcrl">PublishCRL</a>
</td>
<td align="left" width="63%">
Publishes a new CRL.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-publishcrls">PublishCRLs</a>
</td>
<td align="left" width="63%">
Publishes CRLs for the CA.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-resubmitrequest">ResubmitRequest</a>
</td>
<td align="left" width="63%">
Submits a pended certificate request to the policy module.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-revokecertificate">RevokeCertificate</a>
</td>
<td align="left" width="63%">
Revokes a certificate on a specified date.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-setcaproperty">SetCAProperty</a>
</td>
<td align="left" width="63%">
Sets a property value for the CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-setcertificateextension">SetCertificateExtension</a>
</td>
<td align="left" width="63%">
Adds a new extension to a certificate to be issued.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-setconfigentry">SetConfigEntry</a>
</td>
<td align="left" width="63%">
Sets configuration  information for a CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-setrequestattributes">SetRequestAttributes</a>
</td>
<td align="left" width="63%">
Sets the attributes of a certificate request.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
</table> 

