---
UID: NN:certadm.ICertAdmin2
title: ICertAdmin2
author: windows-sdk-content
description: Provide administration functionality for properly authorized clients.
old-location: security\icertadmin2.htm
tech.root: seccrypto
ms.assetid: df40b6ac-825d-4e8d-a80b-6e57a4e740a2
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ICertAdmin2, ICertAdmin2 interface [Security], ICertAdmin2 interface [Security],described, _certsrv_icertadmin2, certadm/ICertAdmin2, security.icertadmin2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# ICertAdmin2 interface


## -description


The <b>ICertAdmin2</b> interface
			is one of two interfaces that provide administration functionality for properly authorized clients.

The <b>ICertAdmin2</b> interface is used to perform the following tasks:
<ul>
<li>Authorize or deny a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a>.</li>
<li>Revoke an issued certificate.</li>
<li>Trigger the generation of a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate revocation list</a> (CRL).</li>
<li>Get the current CRL for the server.</li>
<li>Determine whether a certificate is valid.</li>
<li>Get an archived key.</li>
<li>Get a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) display name, property, or property flag.</li>
<li>Publish one or several CRLs.</li>
<li>Get or set configuration information.</li>
<li>Determine which roles are set.</li>
<li>Import a certificate or key.</li>
</ul>Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertAdmin2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a> and <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>. <b>ICertAdmin2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa383235(v=VS.85).aspx">DeleteRow</a>
</td>
<td align="left" width="63%">
Deletes a row, or set of rows, from a database table.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383236(v=VS.85).aspx">DenyRequest</a>
</td>
<td align="left" width="63%">
Denies a certificate request.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383237(v=VS.85).aspx">GetArchivedKey</a>
</td>
<td align="left" width="63%">
Retrieves an archived key recovery <a href="https://msdn.microsoft.com/en-us/library/ms721569(v=VS.85).aspx">BLOB</a>.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383238(v=VS.85).aspx">GetCAProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383239(v=VS.85).aspx">GetCAPropertyDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for a property.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383240(v=VS.85).aspx">GetCAPropertyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the property flags (denoting data type and indexed status) for a property.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383241(v=VS.85).aspx">GetConfigEntry</a>
</td>
<td align="left" width="63%">
Retrieves configuration  information for a CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383242(v=VS.85).aspx">GetCRL</a>
</td>
<td align="left" width="63%">
Gets a pointer to the current CRL.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383243(v=VS.85).aspx">GetMyRoles</a>
</td>
<td align="left" width="63%">
Retrieves the CA roles of the caller.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383244(v=VS.85).aspx">GetRevocationReason</a>
</td>
<td align="left" width="63%">
Returns a value that specifies the reason a certificate was revoked.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383245(v=VS.85).aspx">ImportCertificate</a>
</td>
<td align="left" width="63%">
Imports a previously issued certificate.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383246(v=VS.85).aspx">ImportKey</a>
</td>
<td align="left" width="63%">
Adds an encrypted key set to an item in the Certificate Services database. The  key set is encrypted to one or several key recovery agent (KRA) certificates.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383247(v=VS.85).aspx">IsValidCertificate</a>
</td>
<td align="left" width="63%">
Checks the validity of a certificate.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383248(v=VS.85).aspx">PublishCRL</a>
</td>
<td align="left" width="63%">
Publishes a new CRL.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383249(v=VS.85).aspx">PublishCRLs</a>
</td>
<td align="left" width="63%">
Publishes CRLs for the CA.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383250(v=VS.85).aspx">ResubmitRequest</a>
</td>
<td align="left" width="63%">
Submits a pended certificate request to the policy module.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383251(v=VS.85).aspx">RevokeCertificate</a>
</td>
<td align="left" width="63%">
Revokes a certificate on a specified date.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383252(v=VS.85).aspx">SetCAProperty</a>
</td>
<td align="left" width="63%">
Sets a property value for the CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383257(v=VS.85).aspx">SetCertificateExtension</a>
</td>
<td align="left" width="63%">
Adds a new extension to a certificate to be issued.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383263(v=VS.85).aspx">SetConfigEntry</a>
</td>
<td align="left" width="63%">
Sets configuration  information for a CA.</p> (Inherited from <b>ICertAdmin2</b><b>CCertAdmin</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383266(v=VS.85).aspx">SetRequestAttributes</a>
</td>
<td align="left" width="63%">
Sets the attributes of a certificate request.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a><b>CCertAdmin</b>)</td>
</tr>
</table> 

