---
UID: NN:certcli.ICertRequest3
title: ICertRequest3 (certcli.h)
description: Provide communications between a client or intermediary application and Certificate Services.helpviewer_keywords: ["ICertRequest3","ICertRequest3 interface [Security]","ICertRequest3 interface [Security]","described","certcli/ICertRequest3","security.icertrequest3"]
old-location: security\icertrequest3.htm
tech.root: SecCrypto
ms.assetid: 01de2ac0-4844-41a6-acef-e3e83b350393
ms.date: 12/05/2018
ms.keywords: ICertRequest3, ICertRequest3 interface [Security], ICertRequest3 interface [Security],described, certcli/ICertRequest3, security.icertrequest3
f1_keywords:
- certcli/ICertRequest3
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertRequest3 interface


## -description


The <b>ICertRequest3</b> interface is one of three interfaces that  provide communications between a client or intermediary application and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">Certificate Services</a>.

Client and intermediary applications can call the  <b>ICertRequest3</b> methods to perform the following tasks:<ul>
<li>Submit a certificate request.</li>
<li>Retrieve the disposition, last status, and identifier of a request.</li>
<li>Retrieve the certificate issued for the request.</li>
<li>Retrieve pending certificates for previous requests.</li>
<li>Retrieve the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) certificate for the Certificate Services server.</li>
<li>Retrieve the CA property value, display name, and any flags associated with the property.</li>
<li>Retrieve the cached response data returned by the server.</li>
<li>Retrieve error message text for an <b>HRESULT</b> error code.</li>
</ul>


<b>ICertRequest3</b> is defined in Certcli.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertRequest3</b> interface. The type information for this interface is also in Certcli.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertRequest3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>, <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>, and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. <b>ICertRequest3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest-getcacertificate">GetCACertificate</a>
</td>
<td align="left" width="63%">
Returns the CA certificate for the Certificate Services server.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest2-getcaproperty">GetCAProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the CA. This method's functionality is identical to 
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcaproperty">ICertAdmin2::GetCAProperty</a>.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest2-getcapropertydisplayname">GetCAPropertyDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for a property. This method's functionality is identical to 
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcapropertydisplayname">ICertAdmin2::GetCAPropertyDisplayName</a>.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest2-getcapropertyflags">GetCAPropertyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the property flags (denoting data type and indexed status) for a property. This method's functionality is identical to 
<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcapropertyflags">ICertAdmin2::GetCAPropertyFlags</a>.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest-getcertificate">GetCertificate</a>
</td>
<td align="left" width="63%">
Returns the certificate issued for the request.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest-getdispositionmessage">GetDispositionMessage</a>
</td>
<td align="left" width="63%">
Gets a human-readable message giving the current disposition of the certificate request.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest2-geterrormessagetext">GetErrorMessageText</a>
</td>
<td align="left" width="63%">
Retrieves message text for a given <b>HRESULT</b> error code.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest2-getfullresponseproperty">GetFullResponseProperty</a>
</td>
<td align="left" width="63%">
Retrieves the cached response data returned by the server.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest2-getissuedcertificate">GetIssuedCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the disposition of a certificate request.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest3-getissuedcertificate2">GetIssuedCertificate2</a>
</td>
<td align="left" width="63%">
Retrieves a certificate's disposition by specifying either the request ID string or the certificate serial number.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest-getlaststatus">GetLastStatus</a>
</td>
<td align="left" width="63%">
Gets the last return code for this request.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest3-getrefreshpolicy">GetRefreshPolicy</a>
</td>
<td align="left" width="63%">
Returns a value that indicates whether a client's cached certificate enrollment policy is out of date and needs to be refreshed.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest-getrequestid">GetRequestId</a>
</td>
<td align="left" width="63%">
Gets the current internal request number for the request and subsequent certificate.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest3-getrequestidstring">GetRequestIdString</a>
</td>
<td align="left" width="63%">
Gets the current internal request number, formatted as a string, for the request and subsequent certificate.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest-retrievepending">RetrievePending</a>
</td>
<td align="left" width="63%">
Attempts to retrieve the certificate issued for an earlier request, that may have initially been made pending.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest3-setcredential">SetCredential</a>
</td>
<td align="left" width="63%">
Sets the credential used to contact the Certificate Enrollment Web Service.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">Submit</a>
</td>
<td align="left" width="63%">
Submits a request to the Certificate Services server.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">CCertRequest</a>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

