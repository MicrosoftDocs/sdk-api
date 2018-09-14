---
UID: NN:certcli.ICertRequest
title: ICertRequest
author: windows-sdk-content
description: Provides communications between a client or intermediary application and Certificate services.
old-location: security\icertrequest.htm
tech.root: seccrypto
ms.assetid: 2f371aa6-492e-41ba-8455-66e9d5f5da44
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICertRequest, ICertRequest interface [Security], ICertRequest interface [Security],described, _certsrv_icertrequest, certcli/ICertRequest, security.icertrequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Certcli.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertRequest interface


## -description


The <b>ICertRequest</b> interface provides communications between a client or intermediary application and Certificate services.

Client and intermediary applications can call the  <b>ICertRequest</b> methods to perform the following tasks:<ul>
<li>Submit certificate request.</li>
<li>Retrieve the disposition, last status, and identifier of a request.</li>
<li>Retrieve the certificate issued for the request.</li>
<li>Retrieve pending certificates for previous requests.</li>
<li>Retrieve the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) certificate for the Certificate Services server.</li>
</ul>


<b>ICertRequest</b> is defined in Certcli.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertRequest</b> interface. The type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertRequest</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertRequest</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICertRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385042(v=VS.85).aspx">GetCACertificate</a>
</td>
<td align="left" width="63%">
Returns the CA certificate for the Certificate Services server.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a><b>ICertRequest</b><a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385046(v=VS.85).aspx">GetCertificate</a>
</td>
<td align="left" width="63%">
Returns the certificate issued for the request.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a><b>ICertRequest</b><a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385047(v=VS.85).aspx">GetDispositionMessage</a>
</td>
<td align="left" width="63%">
Gets a human-readable message giving the current disposition of the certificate request.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a><b>ICertRequest</b><a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385051(v=VS.85).aspx">GetLastStatus</a>
</td>
<td align="left" width="63%">
Gets the last return code for this request.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a><b>ICertRequest</b><a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385052(v=VS.85).aspx">GetRequestId</a>
</td>
<td align="left" width="63%">
Gets the current internal request number for the request and subsequent certificate.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a><b>ICertRequest</b><a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385053(v=VS.85).aspx">RetrievePending</a>
</td>
<td align="left" width="63%">
Attempts to retrieve the certificate issued for an earlier request, that may have initially been made pending.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a><b>ICertRequest</b><a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385054(v=VS.85).aspx">Submit</a>
</td>
<td align="left" width="63%">
Submits a request to the Certificate Services server.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a><b>ICertRequest</b><a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
</table> 

