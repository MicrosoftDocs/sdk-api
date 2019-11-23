---
UID: NN:certif.ICertServerExit
title: ICertServerExit (certif.h)

description: Exported by the server engine and is called by exit modules.
old-location: security\icertserverexit.htm
tech.root: SecCrypto
ms.assetid: 1554c09c-a7c1-44ad-9821-93c0913212fc

ms.date: 12/05/2018
ms.keywords: ICertServerExit, ICertServerExit interface [Security], ICertServerExit interface [Security],described, _certsrv_icertserverexit, certif/ICertServerExit, security.icertserverexit
ms.topic: interface
f1_keywords: 
 - "certif/ICertServerExit"
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
 - ICertServerExit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertServerExit interface


## -description


The <b>ICertServerExit</b> interface is exported by the server engine and is called by exit modules.

<b>ICertServerExit</b> allows exit modules to get and enumerate elements of requests and certificates.

<b>ICertServerExit</b> is defined in Certif.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertServerExit</b> interface. The type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertServerExit</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertServerExit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertServerExit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributes">EnumerateAttributes</a>
</td>
<td align="left" width="63%">
Returns the name of the next request attribute to be enumerated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributesclose">EnumerateAttributesClose</a>
</td>
<td align="left" width="63%">
Frees any resources connected with attribute enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributessetup">EnumerateAttributesSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first attribute associated with the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateextensions">EnumerateExtensions</a>
</td>
<td align="left" width="63%">
Returns the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the next certificate extension to be enumerated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateextensionsclose">EnumerateExtensionsClose</a>
</td>
<td align="left" width="63%">
Frees any resources connected with extension enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateextensionssetup">EnumerateExtensionsSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first certificate extension associated with the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-getcertificateextension">GetCertificateExtension</a>
</td>
<td align="left" width="63%">
Gets a specified certificate extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-getcertificateextensionflags">GetCertificateExtensionFlags</a>
</td>
<td align="left" width="63%">
Gets the flags from the extension acquired by the most recent call to 
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-getcertificateextension">GetCertificateExtension</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-getcertificateproperty">GetCertificateProperty</a>
</td>
<td align="left" width="63%">
Returns a named certificate property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-getrequestattribute">GetRequestAttribute</a>
</td>
<td align="left" width="63%">
Returns a named request attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-getrequestproperty">GetRequestProperty</a>
</td>
<td align="left" width="63%">
Returns a named request property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certif/nf-certif-icertserverexit-setcontext">SetContext</a>
</td>
<td align="left" width="63%">
Sets the current instantiation of the interface to operate on the specified request context.

</td>
</tr>
</table> 

