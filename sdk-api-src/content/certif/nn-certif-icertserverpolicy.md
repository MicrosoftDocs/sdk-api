---
UID: NN:certif.ICertServerPolicy
title: ICertServerPolicy
author: windows-sdk-content
description: Allows the policy module to communicate with Certificate Services.
old-location: security\icertserverpolicy.htm
tech.root: seccrypto
ms.assetid: 7d16161e-9827-46a0-9989-30ebca792bb1
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ICertServerPolicy, ICertServerPolicy interface [Security], ICertServerPolicy interface [Security],described, _certsrv_icertserverpolicy, certif/ICertServerPolicy, security.icertserverpolicy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerPolicy interface


## -description


The <b>ICertServerPolicy</b> interface allows the policy module to communicate with Certificate Services.
<div class="alert"><b>Note</b>  Certificate Services communicates with the policy module through the <a href="https://msdn.microsoft.com/en-us/library/Aa385034(v=VS.85).aspx">ICertPolicy2</a> interface.</div><div> </div>The <b>ICertServerPolicy</b> interface is exported by the server engine and is called by the policy module to perform the following tasks:<ul>
<li>Specify which certificate request  is used as the current context for subsequent operations.</li>
<li>Enumerate and  retrieve the extensions (including extension flags) of a certificate request, and set the extensions of the issued certificate.</li>
<li>Enumerate and retrieve request attributes.</li>
<li>Retrieve certificate request properties.</li>
<li>Retrieve and set certificate properties.</li>
</ul>


From the time the 
<a href="https://msdn.microsoft.com/en-us/library/Aa385039(v=VS.85).aspx">ICertPolicy::VerifyRequest</a> method is called until it returns, the unresolved request and certificate under construction can be accessed through a Context data object. Because the policy module can add to or override request properties by calling 
<a href="https://msdn.microsoft.com/en-us/library/Aa385395(v=VS.85).aspx">ICertServerPolicy::SetCertificateProperty</a>, certificate properties can differ from request properties.

<b>ICertServerPolicy</b> is defined in Certif.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertServerPolicy</b> interface. The type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertServerPolicy</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertServerPolicy</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa385081(v=VS.85).aspx">EnumerateAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current attribute and moves the internal enumeration pointer to the next  attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385082(v=VS.85).aspx">EnumerateAttributesClose</a>
</td>
<td align="left" width="63%">
Frees the  resources connected with attribute enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385083(v=VS.85).aspx">EnumerateAttributesSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first request  <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">attribute</a> associated with the current <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">context</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385084(v=VS.85).aspx">EnumerateExtensions</a>
</td>
<td align="left" width="63%">
Retrieves the OID of the current extension and moves the internal enumeration pointer to the next  extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385085(v=VS.85).aspx">EnumerateExtensionsClose</a>
</td>
<td align="left" width="63%">
Frees the resources connected with extension enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385086(v=VS.85).aspx">EnumerateExtensionsSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first certificate extension associated with the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385087(v=VS.85).aspx">GetCertificateExtension</a>
</td>
<td align="left" width="63%">
Retrieves a specific certificate extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385088(v=VS.85).aspx">GetCertificateExtensionFlags</a>
</td>
<td align="left" width="63%">
Retrieves the  flags associated with the extension acquired by the most recent call to 
<a href="https://msdn.microsoft.com/en-us/library/Aa385087(v=VS.85).aspx">GetCertificateExtension</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385089(v=VS.85).aspx">GetCertificateProperty</a>
</td>
<td align="left" width="63%">
Returns a named certificate property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385090(v=VS.85).aspx">GetRequestAttribute</a>
</td>
<td align="left" width="63%">
Returns a named request attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385091(v=VS.85).aspx">GetRequestProperty</a>
</td>
<td align="left" width="63%">
Retrieves a specific property from a request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385092(v=VS.85).aspx">SetCertificateExtension</a>
</td>
<td align="left" width="63%">
Adds a new extension to the certificate to be issued for the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385395(v=VS.85).aspx">SetCertificateProperty</a>
</td>
<td align="left" width="63%">
Causes the server engine to add a named property to a certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa385398(v=VS.85).aspx">SetContext</a>
</td>
<td align="left" width="63%">
Specifies the certificate request  to be used as the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">context</a> for subsequent calls to Certificate Services.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383250(v=VS.85).aspx">ICertAdmin::ResubmitRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383266(v=VS.85).aspx">ICertAdmin::SetRequestAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385039(v=VS.85).aspx">ICertPolicy::VerifyRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385054(v=VS.85).aspx">ICertRequest::Submit</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

