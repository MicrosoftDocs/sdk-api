---
UID: NN:certif.ICertServerPolicy
title: ICertServerPolicy
author: windows-sdk-content
description: Allows the policy module to communicate with Certificate Services.
old-location: security\icertserverpolicy.htm
old-project: SecCrypto
ms.assetid: 7d16161e-9827-46a0-9989-30ebca792bb1
ms.author: windowssdkdev
ms.date: 06/04/2018
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
tech.root: 
req.typenames: X509RequestType
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
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
---

# ICertServerPolicy interface


## -description


The <b>ICertServerPolicy</b> interface allows the policy module to communicate with Certificate Services.
<div class="alert"><b>Note</b>  Certificate Services communicates with the policy module through the <a href="https://msdn.microsoft.com/2e48b096-e23a-4106-bfaf-f089d2291fba">ICertPolicy2</a> interface.</div><div> </div>The <b>ICertServerPolicy</b> interface is exported by the server engine and is called by the policy module to perform the following tasks:<ul>
<li>Specify which certificate request  is used as the current context for subsequent operations.</li>
<li>Enumerate and  retrieve the extensions (including extension flags) of a certificate request, and set the extensions of the issued certificate.</li>
<li>Enumerate and retrieve request attributes.</li>
<li>Retrieve certificate request properties.</li>
<li>Retrieve and set certificate properties.</li>
</ul>


From the time the 
<a href="https://msdn.microsoft.com/860f0eb0-5b23-44bd-8416-687a94962f1b">ICertPolicy::VerifyRequest</a> method is called until it returns, the unresolved request and certificate under construction can be accessed through a Context data object. Because the policy module can add to or override request properties by calling 
<a href="https://msdn.microsoft.com/1230aa79-d8b0-4f2b-ab10-412b8c530b0b">ICertServerPolicy::SetCertificateProperty</a>, certificate properties can differ from request properties.

<b>ICertServerPolicy</b> is defined in Certif.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertServerPolicy</b> interface. The type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertServerPolicy</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertServerPolicy</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5db05ed9-ab17-462b-9a76-34458489771a">EnumerateAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current attribute and moves the internal enumeration pointer to the next  attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91cb8edd-7735-44c5-b2c5-d46fa1e33e41">EnumerateAttributesClose</a>
</td>
<td align="left" width="63%">
Frees the  resources connected with attribute enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14b81b88-36db-4b01-96e6-eafed22ae02e">EnumerateAttributesSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first request  <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> associated with the current <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/565ff4d5-0d22-466d-8458-f98b992a1868">EnumerateExtensions</a>
</td>
<td align="left" width="63%">
Retrieves the OID of the current extension and moves the internal enumeration pointer to the next  extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1755fc5-f18f-45b5-a89a-44c6598c0e2c">EnumerateExtensionsClose</a>
</td>
<td align="left" width="63%">
Frees the resources connected with extension enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7ad32a5-d7df-407f-8efe-c9931610c2d2">EnumerateExtensionsSetup</a>
</td>
<td align="left" width="63%">
Initializes the internal enumeration pointer to the first certificate extension associated with the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2c8e1d5-6ddb-4c8f-8052-f45cd52e2bef">GetCertificateExtension</a>
</td>
<td align="left" width="63%">
Retrieves a specific certificate extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6266e96d-81da-478f-99da-86936b4cfc6b">GetCertificateExtensionFlags</a>
</td>
<td align="left" width="63%">
Retrieves the  flags associated with the extension acquired by the most recent call to 
<a href="https://msdn.microsoft.com/e2c8e1d5-6ddb-4c8f-8052-f45cd52e2bef">GetCertificateExtension</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7ece535-31c7-4468-a9ef-84f4dbf16d76">GetCertificateProperty</a>
</td>
<td align="left" width="63%">
Returns a named certificate property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/344cb710-4824-455c-9599-3036a2b36905">GetRequestAttribute</a>
</td>
<td align="left" width="63%">
Returns a named request attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4055008a-7034-47f3-bbae-c870165ab3ef">GetRequestProperty</a>
</td>
<td align="left" width="63%">
Retrieves a specific property from a request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aed8b621-3881-41fe-b7a3-657fecdab351">SetCertificateExtension</a>
</td>
<td align="left" width="63%">
Adds a new extension to the certificate to be issued for the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1230aa79-d8b0-4f2b-ab10-412b8c530b0b">SetCertificateProperty</a>
</td>
<td align="left" width="63%">
Causes the server engine to add a named property to a certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556644">SetContext</a>
</td>
<td align="left" width="63%">
Specifies the certificate request  to be used as the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a> for subsequent calls to Certificate Services.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/610712d9-3661-42ba-9d2f-27862ba8dbd4">ICertAdmin::ResubmitRequest</a>



<a href="https://msdn.microsoft.com/309c53f9-50cf-4c50-bc48-a4f15a8ced18">ICertAdmin::SetRequestAttributes</a>



<a href="https://msdn.microsoft.com/860f0eb0-5b23-44bd-8416-687a94962f1b">ICertPolicy::VerifyRequest</a>



<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">ICertRequest</a>



<a href="https://msdn.microsoft.com/22ae8d39-3f16-4f7d-94a0-aa68b03aaa0b">ICertRequest::Submit</a>



<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

