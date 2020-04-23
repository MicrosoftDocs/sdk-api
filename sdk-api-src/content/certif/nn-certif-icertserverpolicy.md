---
UID: NN:certif.ICertServerPolicy
title: ICertServerPolicy (certif.h)
description: Allows the policy module to communicate with Certificate Services.helpviewer_keywords: ["ICertServerPolicy","ICertServerPolicy interface [Security]","ICertServerPolicy interface [Security]","described","_certsrv_icertserverpolicy","certif/ICertServerPolicy","security.icertserverpolicy"]
old-location: security\icertserverpolicy.htm
tech.root: SecCrypto
ms.assetid: 7d16161e-9827-46a0-9989-30ebca792bb1
ms.date: 12/05/2018
ms.keywords: ICertServerPolicy, ICertServerPolicy interface [Security], ICertServerPolicy interface [Security],described, _certsrv_icertserverpolicy, certif/ICertServerPolicy, security.icertserverpolicy
f1_keywords:
- certif/ICertServerPolicy
dev_langs:
- c++
req.header: certif.h
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
- ICertServerPolicy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertServerPolicy interface


## -description


The <b>ICertServerPolicy</b> interface allows the policy module to communicate with Certificate Services.
<div class="alert"><b>Note</b>  Certificate Services communicates with the policy module through the <a href="https://docs.microsoft.com/windows/desktop/api/certpol/nn-certpol-icertpolicy2">ICertPolicy2</a> interface.</div><div> </div>The <b>ICertServerPolicy</b> interface is exported by the server engine and is called by the policy module to perform the following tasks:<ul>
<li>Specify which certificate request  is used as the current context for subsequent operations.</li>
<li>Enumerate and  retrieve the extensions (including extension flags) of a certificate request, and set the extensions of the issued certificate.</li>
<li>Enumerate and retrieve request attributes.</li>
<li>Retrieve certificate request properties.</li>
<li>Retrieve and set certificate properties.</li>
</ul>


From the time the 
<a href="https://docs.microsoft.com/windows/desktop/api/certpol/nf-certpol-icertpolicy-verifyrequest">ICertPolicy::VerifyRequest</a> method is called until it returns, the unresolved request and certificate under construction can be accessed through a Context data object. Because the policy module can add to or override request properties by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcertificateproperty">ICertServerPolicy::SetCertificateProperty</a>, certificate properties can differ from request properties.

<b>ICertServerPolicy</b> is defined in Certif.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertServerPolicy</b> interface. The type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertServerPolicy</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertServerPolicy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertServerPolicy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateattributes">EnumerateAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current attribute and moves the internal enumeration pointer to the next  attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateattributesclose">EnumerateAttributesClose</a>
</td>
<td align="left" width="63%">
Frees the  resources connected with attribute enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateattributessetup">EnumerateAttributesSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first request  <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">attribute</a> associated with the current <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">context</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateextensions">EnumerateExtensions</a>
</td>
<td align="left" width="63%">
Retrieves the OID of the current extension and moves the internal enumeration pointer to the next  extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateextensionsclose">EnumerateExtensionsClose</a>
</td>
<td align="left" width="63%">
Frees the resources connected with extension enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateextensionssetup">EnumerateExtensionsSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first certificate extension associated with the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-getcertificateextension">GetCertificateExtension</a>
</td>
<td align="left" width="63%">
Retrieves a specific certificate extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-getcertificateextensionflags">GetCertificateExtensionFlags</a>
</td>
<td align="left" width="63%">
Retrieves the  flags associated with the extension acquired by the most recent call to 
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-getcertificateextension">GetCertificateExtension</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-getcertificateproperty">GetCertificateProperty</a>
</td>
<td align="left" width="63%">
Returns a named certificate property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-getrequestattribute">GetRequestAttribute</a>
</td>
<td align="left" width="63%">
Returns a named request attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-getrequestproperty">GetRequestProperty</a>
</td>
<td align="left" width="63%">
Retrieves a specific property from a request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcertificateextension">SetCertificateExtension</a>
</td>
<td align="left" width="63%">
Adds a new extension to the certificate to be issued for the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcertificateproperty">SetCertificateProperty</a>
</td>
<td align="left" width="63%">
Causes the server engine to add a named property to a certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">SetContext</a>
</td>
<td align="left" width="63%">
Specifies the certificate request  to be used as the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">context</a> for subsequent calls to Certificate Services.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-resubmitrequest">ICertAdmin::ResubmitRequest</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certadm/nf-certadm-icertadmin-setrequestattributes">ICertAdmin::SetRequestAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certpol/nf-certpol-icertpolicy-verifyrequest">ICertPolicy::VerifyRequest</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">ICertRequest::Submit</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

