---
UID: NN:certcli.ICertRequest3
title: ICertRequest3
author: windows-sdk-content
description: Provide communications between a client or intermediary application and Certificate Services.
old-location: security\icertrequest3.htm
tech.root: seccrypto
ms.assetid: 01de2ac0-4844-41a6-acef-e3e83b350393
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ICertRequest3, ICertRequest3 interface [Security], ICertRequest3 interface [Security],described, certcli/ICertRequest3, security.icertrequest3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certcli.h
req.include-header: Certsrv.h
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
 - ICertRequest3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertRequest3 interface


## -description


The <b>ICertRequest3</b> interface is one of three interfaces that  provide communications between a client or intermediary application and <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">Certificate Services</a>.

Client and intermediary applications can call the  <b>ICertRequest3</b> methods to perform the following tasks:<ul>
<li>Submit a certificate request.</li>
<li>Retrieve the disposition, last status, and identifier of a request.</li>
<li>Retrieve the certificate issued for the request.</li>
<li>Retrieve pending certificates for previous requests.</li>
<li>Retrieve the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) certificate for the Certificate Services server.</li>
<li>Retrieve the CA property value, display name, and any flags associated with the property.</li>
<li>Retrieve the cached response data returned by the server.</li>
<li>Retrieve error message text for an <b>HRESULT</b> error code.</li>
</ul>


<b>ICertRequest3</b> is defined in Certcli.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertRequest3</b> interface. The type information for this interface is also in Certcli.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertRequest3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>. <b>ICertRequest3</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICertRequest3</b> interface has these methods.
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
Returns the CA certificate for the Certificate Services server.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385043(v=VS.85).aspx">GetCAProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the CA. This method's functionality is identical to 
<a href="https://msdn.microsoft.com/en-us/library/Aa383238(v=VS.85).aspx">ICertAdmin2::GetCAProperty</a>.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385044(v=VS.85).aspx">GetCAPropertyDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for a property. This method's functionality is identical to 
<a href="https://msdn.microsoft.com/en-us/library/Aa383239(v=VS.85).aspx">ICertAdmin2::GetCAPropertyDisplayName</a>.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385045(v=VS.85).aspx">GetCAPropertyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the property flags (denoting data type and indexed status) for a property. This method's functionality is identical to 
<a href="https://msdn.microsoft.com/en-us/library/Aa383240(v=VS.85).aspx">ICertAdmin2::GetCAPropertyFlags</a>.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385046(v=VS.85).aspx">GetCertificate</a>
</td>
<td align="left" width="63%">
Returns the certificate issued for the request.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385047(v=VS.85).aspx">GetDispositionMessage</a>
</td>
<td align="left" width="63%">
Gets a human-readable message giving the current disposition of the certificate request.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385048(v=VS.85).aspx">GetErrorMessageText</a>
</td>
<td align="left" width="63%">
Retrieves message text for a given <b>HRESULT</b> error code.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385049(v=VS.85).aspx">GetFullResponseProperty</a>
</td>
<td align="left" width="63%">
Retrieves the cached response data returned by the server.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385050(v=VS.85).aspx">GetIssuedCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the disposition of a certificate request.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee373778(v=VS.85).aspx">GetIssuedCertificate2</a>
</td>
<td align="left" width="63%">
Retrieves a certificate's disposition by specifying either the request ID string or the certificate serial number.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385051(v=VS.85).aspx">GetLastStatus</a>
</td>
<td align="left" width="63%">
Gets the last return code for this request.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee373779(v=VS.85).aspx">GetRefreshPolicy</a>
</td>
<td align="left" width="63%">
Returns a value that indicates whether a client's cached certificate enrollment policy is out of date and needs to be refreshed.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385052(v=VS.85).aspx">GetRequestId</a>
</td>
<td align="left" width="63%">
Gets the current internal request number for the request and subsequent certificate.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee373780(v=VS.85).aspx">GetRequestIdString</a>
</td>
<td align="left" width="63%">
Gets the current internal request number, formatted as a string, for the request and subsequent certificate.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385053(v=VS.85).aspx">RetrievePending</a>
</td>
<td align="left" width="63%">
Attempts to retrieve the certificate issued for an earlier request, that may have initially been made pending.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee373781(v=VS.85).aspx">SetCredential</a>
</td>
<td align="left" width="63%">
Sets the credential used to contact the Certificate Enrollment Web Service.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385054(v=VS.85).aspx">Submit</a>
</td>
<td align="left" width="63%">
Submits a request to the Certificate Services server.</p> (Inherited from <a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">CCertRequest</a>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

